# cream-docker-bs
Build system for CREAM based on Docker

## Howto build the stack

- `docker build -t devel-base:<distro> -f Dockerfile-devel-base .`
- `docker build -t service-base:<distro> -f Dockerfile-service-base --build-arg jdlapij_version=jdl-api-java_R_*_*_*_* --build-arg cream_utils_version=cream-utils_R_*_*_*_* .`
- `docker build -t cream-service:<distro> -f Dockerfile-cream-service --build-arg cream_common_version=cream-common_R_*_*_*_* --build-arg cream_api_version=cream-api-java_R_*_*_*_* --build-arg cream_version=cream_R_*_*_*_* --build-arg canl_tomcat_version=canl-java-tomcat_R_*_*_*_* --build-arg blah_version=v*.*.* .`
- `docker build -t infosystem:<distro> -f Dockerfile-infosystem --build-arg info_generic_version=dynsched-generic_*_*_*_*  --build-arg info_pbs_version=dynsched-pbs_*_*_*_*  --build-arg info_slurm_version=info-dynamic-scheduler-slurm_R_*_*_*_* --build-arg info_lsf_version=v*.*.*-* --build-arg info_condor_version=v*.*.8 .`
- `docker build -t ui-base:<distro> -f Dockerfile-ui-base --build-arg jobman_exc_version=jobman-exception_R_*_*_*_* --build-arg classad_utils_version=classad-utils_R_*_*_*_* .`
- `docker build -t ui-client:<distro> -f Dockerfile-ui-client --build-arg jdl_apic_version=jdl-api-cpp_R_*_*_*_* --build-arg cream_apic_version=cream-client-api-c_R_*_*_*_* --build-arg cream_cli_version=cream-cli_R_*_*_*_* .`
