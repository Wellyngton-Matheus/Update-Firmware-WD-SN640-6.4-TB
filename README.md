# Atualiza-o-de-Firmware-WD-SN640-6.4-TB
Procedimento documentado para atualização do firmware R121000A para R121000B em SSDs WD SN640 6.4 TB (WUS4CB064D7P3E3) utilizados em servidores Cisco UCS S3260, incluindo extração, decriptação, validação da assinatura e atualização do firmware via NVMe.

# WD SN640 R121000B Firmware Update

Procedimento documentado para atualização do firmware de SSDs **WD SN640 6.4 TB** utilizados em servidores **Cisco UCS S3260**.

O procedimento foi validado para o modelo:

- **Model:** `WUS4CB064D7P3E3`
- **Firmware original:** `R121000A`
- **Firmware alvo:** `R121000B`
- **Capacity:** 6.4 TB
- **Vendor ID:** `0x1B96`
- **Subsystem Vendor ID:** `0x1137`
- **Cisco HUU:** `4.3.6.260054`

---

## ⚠️ Avisos importantes

> **Este procedimento foi validado em um SSD WD SN640 6.4 TB.**
>
> Antes de executar o procedimento em produção, confirme o modelo e o firmware do SSD.

O procedimento modifica o firmware do dispositivo. Uma atualização incorreta pode deixar o dispositivo indisponível.

**Faça backup dos dados e tenha um procedimento de recuperação antes de realizar a atualização.**

O `imgverify` utilizado neste procedimento é **destrutivo sobre o arquivo informado**: durante a validação ele remove o cabeçalho e a assinatura do pacote. Portanto, mantenha uma cópia do arquivo decriptado original.
