# ParticlePoolCrash

Developed with Unreal Engine 4

Basic project to demonstrate crash with nigara particle systems using pools. 

Reproduction steps for crash. 
1. Package a shipping client build for windows-64 bit
2. Start a dedicated server (using the runserver.cmd)
3. Run two or more clients against the server
4. Press connect
5. press spacebar to start spawning particles
6. Wait for crash (should happen within a minute) 




Unhandled Exception: EXCEPTION_ACCESS_VIOLATION 0xffffffff

ParticlePoolCrash_Win64_Shipping!UActorComponent::RegisterComponentWithWorld()
ParticlePoolCrash_Win64_Shipping!UNiagaraFunctionLibrary::SpawnSystemAtLocation()
ParticlePoolCrash_Win64_Shipping!UNiagaraFunctionLibrary::execSpawnSystemAtLocation()
ParticlePoolCrash_Win64_Shipping!UObject::execLetObj()
ParticlePoolCrash_Win64_Shipping!ProcessLocalScriptFunction()
ParticlePoolCrash_Win64_Shipping!ProcessScriptFunction<void (__cdecl*)(UObject * __ptr64,FFrame & __ptr64,void * __ptr64)>()
ParticlePoolCrash_Win64_Shipping!UObject::execLocalFinalFunction()
ParticlePoolCrash_Win64_Shipping!ProcessLocalScriptFunction()
ParticlePoolCrash_Win64_Shipping!UObject::ProcessInternal()
ParticlePoolCrash_Win64_Shipping!UFunction::Invoke()
ParticlePoolCrash_Win64_Shipping!UObject::ProcessEvent()
ParticlePoolCrash_Win64_Shipping!AActor::ProcessEvent()
ParticlePoolCrash_Win64_Shipping!FObjectReplicator::ReceivedRPC()
ParticlePoolCrash_Win64_Shipping!FObjectReplicator::ReceivedBunch()
ParticlePoolCrash_Win64_Shipping!UActorChannel::ProcessBunch()
ParticlePoolCrash_Win64_Shipping!UActorChannel::ReceivedBunch()
ParticlePoolCrash_Win64_Shipping!UChannel::ReceivedNextBunch()
ParticlePoolCrash_Win64_Shipping!UChannel::ReceivedRawBunch()
ParticlePoolCrash_Win64_Shipping!UNetConnection::ReceivedPacket()
ParticlePoolCrash_Win64_Shipping!UNetConnection::ReceivedRawPacket()
ParticlePoolCrash_Win64_Shipping!UIpNetDriver::TickDispatch()
ParticlePoolCrash_Win64_Shipping!TBaseUObjectMethodDelegateInstance<0,AArchVisCharacter,void __cdecl(float)>::ExecuteIfSafe()
ParticlePoolCrash_Win64_Shipping!TBaseMulticastDelegate<void,float>::Broadcast()
ParticlePoolCrash_Win64_Shipping!UWorld::Tick()
ParticlePoolCrash_Win64_Shipping!UGameEngine::Tick()
ParticlePoolCrash_Win64_Shipping!FEngineLoop::Tick()
ParticlePoolCrash_Win64_Shipping!GuardedMain()
ParticlePoolCrash_Win64_Shipping!GuardedMainWrapper()
ParticlePoolCrash_Win64_Shipping!WinMain()
ParticlePoolCrash_Win64_Shipping!__scrt_common_main_seh() [d:\A01\_work\6\s\src\vctools\crt\vcstartup\src\startup\exe_common.inl:288]
kernel32
ntdll

