# Data Quality Report

Gerado em: 2026-10-21T16:34:27.024822+00:00
Status geral: ⚠️ COM FALHAS

## Saída do dbt test

```
[0m16:34:13  Running with dbt=1.8.9
[0m16:34:13  Registered adapter: duckdb=1.8.4
[0m16:34:15  Found 8 models, 16 data tests, 2 seeds, 4 sources, 543 macros
[0m16:34:15  
[0m16:34:16  Concurrency: 1 threads (target='dev')
[0m16:34:16  
[0m16:34:16  1 of 16 START test accepted_values_stg_anp_precos_semanal_produto__GASOLINA_COMUM__GASOLINA_ADITIVADA__ETANOL_HIDRATADO__OLEO_DIESEL__OLEO_DIESEL_S10__GLP__GNV  [RUN]
[0m16:34:17  1 of 16 PASS accepted_values_stg_anp_precos_semanal_produto__GASOLINA_COMUM__GASOLINA_ADITIVADA__ETANOL_HIDRATADO__OLEO_DIESEL__OLEO_DIESEL_S10__GLP__GNV  [[32mPASS[0m in 0.47s]
[0m16:34:17  2 of 16 START test accepted_values_stg_ibge_municipios_uf_sigla__AC__AL__AP__AM__BA__CE__DF__ES__GO__MA__MT__MS__MG__PA__PB__PR__PE__PI__RJ__RN__RS__RO__RR__SC__SP__SE__TO  [RUN]
[0m16:34:17  2 of 16 PASS accepted_values_stg_ibge_municipios_uf_sigla__AC__AL__AP__AM__BA__CE__DF__ES__GO__MA__MT__MS__MG__PA__PB__PR__PE__PI__RJ__RN__RS__RO__RR__SC__SP__SE__TO  [[32mPASS[0m in 0.45s]
[0m16:34:17  3 of 16 START test assert_geo_match_rate ....................................... [RUN]
[0m16:34:18  3 of 16 PASS assert_geo_match_rate ............................................. [[32mPASS[0m in 0.81s]
[0m16:34:18  4 of 16 START test assert_price_range_plausible ................................ [RUN]
[0m16:34:20  4 of 16 PASS assert_price_range_plausible ...................................... [[32mPASS[0m in 1.41s]
[0m16:34:20  5 of 16 START test not_null_mart_dispersao_municipio_codigo_ibge ............... [RUN]
[0m16:34:20  5 of 16 PASS not_null_mart_dispersao_municipio_codigo_ibge ..................... [[32mPASS[0m in 0.23s]
[0m16:34:20  6 of 16 START test not_null_mart_preco_medio_uf_semanal_produto ................ [RUN]
[0m16:34:20  6 of 16 PASS not_null_mart_preco_medio_uf_semanal_produto ...................... [[32mPASS[0m in 0.24s]
[0m16:34:20  7 of 16 START test not_null_mart_preco_medio_uf_semanal_uf_sigla ............... [RUN]
[0m16:34:20  7 of 16 PASS not_null_mart_preco_medio_uf_semanal_uf_sigla ..................... [[32mPASS[0m in 0.25s]
[0m16:34:20  8 of 16 START test not_null_municipio_exceptions_codigo_ibge ................... [RUN]
[0m16:34:21  8 of 16 PASS not_null_municipio_exceptions_codigo_ibge ......................... [[32mPASS[0m in 0.25s]
[0m16:34:21  9 of 16 START test not_null_municipio_exceptions_nome_anp_normalizado .......... [RUN]
[0m16:34:21  9 of 16 PASS not_null_municipio_exceptions_nome_anp_normalizado ................ [[32mPASS[0m in 0.31s]
[0m16:34:21  10 of 16 START test not_null_stg_anp_precos_semanal_data_inicial ............... [RUN]
[0m16:34:21  10 of 16 PASS not_null_stg_anp_precos_semanal_data_inicial ..................... [[32mPASS[0m in 0.36s]
[0m16:34:21  11 of 16 START test not_null_stg_anp_precos_semanal_preco_medio_revenda ........ [RUN]
[0m16:34:22  11 of 16 PASS not_null_stg_anp_precos_semanal_preco_medio_revenda .............. [[32mPASS[0m in 0.41s]
[0m16:34:22  12 of 16 START test not_null_stg_anp_precos_semanal_produto .................... [RUN]
[0m16:34:23  12 of 16 PASS not_null_stg_anp_precos_semanal_produto .......................... [[32mPASS[0m in 1.36s]
[0m16:34:23  13 of 16 START test not_null_stg_ibge_municipios_codigo_ibge ................... [RUN]
[0m16:34:23  13 of 16 PASS not_null_stg_ibge_municipios_codigo_ibge ......................... [[32mPASS[0m in 0.37s]
[0m16:34:23  14 of 16 START test not_null_stg_ibge_municipios_nome_municipio_normalizado .... [RUN]
[0m16:34:24  14 of 16 PASS not_null_stg_ibge_municipios_nome_municipio_normalizado .......... [[32mPASS[0m in 0.35s]
[0m16:34:24  15 of 16 START test not_null_stg_ibge_municipios_uf_sigla ...................... [RUN]
[0m16:34:24  15 of 16 PASS not_null_stg_ibge_municipios_uf_sigla ............................ [[32mPASS[0m in 0.36s]
[0m16:34:24  16 of 16 START test unique_stg_ibge_municipios_codigo_ibge ..................... [RUN]
[0m16:34:24  16 of 16 FAIL 5571 unique_stg_ibge_municipios_codigo_ibge ...................... [[31mFAIL 5571[0m in 0.35s]
[0m16:34:25  
[0m16:34:25  Finished running 16 data tests in 0 hours 0 minutes and 9.21 seconds (9.21s).
[0m16:34:25  
[0m16:34:25  [31mCompleted with 1 error and 0 warnings:[0m
[0m16:34:25  
[0m16:34:25  [31mFailure in test unique_stg_ibge_municipios_codigo_ibge (models/staging/schema.yml)[0m
[0m16:34:25    Got 5571 results, configured to fail if != 0
[0m16:34:25  
[0m16:34:25    compiled code at target/compiled/fuel_lakehouse/models/staging/schema.yml/unique_stg_ibge_municipios_codigo_ibge.sql
[0m16:34:25  
[0m16:34:25    See test failures:
  -----------------------------------------------------------------------------------------
  select * from "warehouse"."main_dbt_test__audit"."unique_stg_ibge_municipios_codigo_ibge"
  -----------------------------------------------------------------------------------------
[0m16:34:25  
[0m16:34:25  Done. PASS=15 WARN=0 ERROR=1 SKIP=0 TOTAL=16

```
