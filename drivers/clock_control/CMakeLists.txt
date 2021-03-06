# SPDX-License-Identifier: Apache-2.0

zephyr_sources_ifdef(CONFIG_CLOCK_CONTROL_BEETLE              beetle_clock_control.c)
zephyr_sources_ifdef(CONFIG_CLOCK_CONTROL_MCUX_CCM            clock_control_mcux_ccm.c)
zephyr_sources_ifdef(CONFIG_CLOCK_CONTROL_MCUX_SIM            clock_control_mcux_sim.c)
zephyr_sources_ifdef(CONFIG_CLOCK_CONTROL_NRF                 nrf_power_clock.c)
zephyr_sources_ifdef(CONFIG_CLOCK_CONTROL_QUARK_SE            quark_se_clock_control.c)
zephyr_sources_ifdef(CONFIG_CLOCK_CONTROL_RV32M1_PCC          clock_control_rv32m1_pcc.c)

if(CONFIG_CLOCK_CONTROL_STM32_CUBE)
  zephyr_sources(stm32_ll_clock.c)

  zephyr_sources_ifdef(CONFIG_SOC_SERIES_STM32F0X stm32f0x_ll_clock.c)
  zephyr_sources_ifdef(CONFIG_SOC_SERIES_STM32F1X stm32f1x_ll_clock.c)
  zephyr_sources_ifdef(CONFIG_SOC_SERIES_STM32F2X stm32f2x_ll_clock.c)
  zephyr_sources_ifdef(CONFIG_SOC_SERIES_STM32F3X stm32f3x_ll_clock.c)
  zephyr_sources_ifdef(CONFIG_SOC_SERIES_STM32F4X stm32f4x_ll_clock.c)
  zephyr_sources_ifdef(CONFIG_SOC_SERIES_STM32F7X stm32f7x_ll_clock.c)
  zephyr_sources_ifdef(CONFIG_SOC_SERIES_STM32L0X stm32l0x_ll_clock.c)
  zephyr_sources_ifdef(CONFIG_SOC_SERIES_STM32L4X stm32l4x_ll_clock.c)
endif()
