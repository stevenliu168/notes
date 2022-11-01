git问题单号/git commit模板（新建 个目录，保存这个，将.gitconfig，.gitmsg_sh放到一个目录）


# notes
notes

ppp 敏捷软件开发:原则、模式与实践
clean code
测试驱动开发 author:kent beck


https://blog.csdn.net/charleslei/article/details/105761627
cuInit(0);
CUdevice cuDevice = 0;
cuDeviceGet(&cuDevice, 0);
CUcontext cuContext = NULL;
cuCtxCreate(&cuContext, CU_CTX_SCHED_BLOCKING_SYNC, cuDevice);
 
NV_ENCODE_API_FUNCTION_LIST nvenc = { NV_ENCODE_API_FUNCTION_LIST_VER };
NVENCSTATUS nvStatus = NvEncodeAPICreateInstance(&nvenc);
 
NV_ENC_OPEN_ENCODE_SESSION_EX_PARAMS encodeSessionExParams = {         
NV_ENC_OPEN_ENCODE_SESSION_EX_PARAMS_VER };
encodeSessionExParams.device     = cuContext;
encodeSessionExParams.deviceType = NV_ENC_DEVICE_TYPE_CUDA;
encodeSessionExParams.apiVersion = NVENCAPI_VERSION;
 
printf("OpenEncodeSesionEx #1\n");
void *hEncoder1 = NULL;
nvStatus = nvenc.nvEncOpenEncodeSessionEx(&encodeSessionExParams, &hEncoder1);
 
printf("OpenEncodeSesionEx #2\n");
void *hEncoder2 = NULL;
nvStatus = nvenc.nvEncOpenEncodeSessionEx(&encodeSessionExParams, &hEncoder2);
 
printf("OpenEncodeSesionEx #3\n");
void *hEncoder3 = NULL;
nvStatus = nvenc.nvEncOpenEncodeSessionEx(&encodeSessionExParams, &hEncoder3);






























