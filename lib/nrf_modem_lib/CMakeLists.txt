#
# Copyright (c) 2018 Nordic Semiconductor
#
# SPDX-License-Identifier: LicenseRef-Nordic-5-Clause
#

zephyr_library()
zephyr_library_sources(nrf_modem_lib.c)
zephyr_library_sources(nrf_modem_os.c)
zephyr_library_sources_ifdef(CONFIG_NET_SOCKETS nrf91_sockets.c)

if(CONFIG_NRF_MODEM_LIB_TRACE)
  zephyr_library_sources(nrf_modem_lib_trace.c)
  add_subdirectory(trace_backends)
endif()

zephyr_library_sources(fault.c)
zephyr_library_sources(sanity.c)

zephyr_linker_sources(RODATA nrf_modem_lib.ld)
