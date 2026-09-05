# ChipDeviceCtrl.py API

* [matter.ChipDeviceCtrl](#matter.ChipDeviceCtrl)
  * [RegisterOnActiveCallback](#matter.ChipDeviceCtrl.RegisterOnActiveCallback)
  * [UnregisterOnActiveCallback](#matter.ChipDeviceCtrl.UnregisterOnActiveCallback)
  * [WaitForCheckIn](#matter.ChipDeviceCtrl.WaitForCheckIn)
  * [CallbackContext](#matter.ChipDeviceCtrl.CallbackContext)
  * [CommissioningContext](#matter.ChipDeviceCtrl.CommissioningContext)
  * [CommissionableNode](#matter.ChipDeviceCtrl.CommissionableNode)
    * [Commission](#matter.ChipDeviceCtrl.CommissionableNode.Commission)
  * [DeviceProxyWrapper](#matter.ChipDeviceCtrl.DeviceProxyWrapper)
  * [ChipDeviceControllerBase](#matter.ChipDeviceCtrl.ChipDeviceControllerBase)
    * [Shutdown](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.Shutdown)
    * [ShutdownAll](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.ShutdownAll)
    * [CheckIsActive](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.CheckIsActive)
    * [IsConnected](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.IsConnected)
    * [ConnectBLE](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.ConnectBLE)
    * [ConnectNFC](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.ConnectNFC)
    * [ContinueCommissioningAfterConnectNetworkRequest](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.ContinueCommissioningAfterConnectNetworkRequest)
    * [UnpairDevice](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.UnpairDevice)
    * [CloseBLEConnection](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.CloseBLEConnection)
    * [ExpireSessions](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.ExpireSessions)
    * [MarkSessionDefunct](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.MarkSessionDefunct)
    * [StopPairing](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.StopPairing)
    * [MarkSessionForEviction](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.MarkSessionForEviction)
    * [DeleteAllSessionResumptionStorage](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.DeleteAllSessionResumptionStorage)
    * [SetLocalMRPConfig](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetLocalMRPConfig)
    * [ResetLocalMRPConfig](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.ResetLocalMRPConfig)
    * [EstablishPASESessionBLE](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.EstablishPASESessionBLE)
    * [EstablishPASESessionIP](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.EstablishPASESessionIP)
    * [EstablishPASESessionThreadMeshcop](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.EstablishPASESessionThreadMeshcop)
    * [EstablishPASESession](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.EstablishPASESession)
    * [GetTestCommissionerUsed](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetTestCommissionerUsed)
    * [SetTestCommissionerSimulateFailureOnStage](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetTestCommissionerSimulateFailureOnStage)
    * [SetTestCommissionerSimulateFailureOnReport](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetTestCommissionerSimulateFailureOnReport)
    * [SetTestCommissionerPrematureCompleteAfter](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetTestCommissionerPrematureCompleteAfter)
    * [CheckTestCommissionerCallbacks](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.CheckTestCommissionerCallbacks)
    * [CheckStageSuccessful](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.CheckStageSuccessful)
    * [CheckTestCommissionerPaseConnection](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.CheckTestCommissionerPaseConnection)
    * [ResolveNode](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.ResolveNode)
    * [GetAddressAndPort](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetAddressAndPort)
    * [GetLastThreadMeshcopDiscoveryDiagnostic](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetLastThreadMeshcopDiscoveryDiagnostic)
    * [DiscoverCommissionableNodes](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.DiscoverCommissionableNodes)
    * [GetDiscoveredDevices](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetDiscoveredDevices)
    * [GetIPForDiscoveredDevice](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetIPForDiscoveredDevice)
    * [OpenCommissioningWindow](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.OpenCommissioningWindow)
    * [OpenJointCommissioningWindow](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.OpenJointCommissioningWindow)
    * [GetCompressedFabricId](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetCompressedFabricId)
    * [GetFabricIdInternal](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetFabricIdInternal)
    * [GetFabricIndexInternal](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetFabricIndexInternal)
    * [GetNodeIdInternal](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetNodeIdInternal)
    * [GetRootPublicKeyBytesInternal](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetRootPublicKeyBytesInternal)
    * [GetClusterHandler](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetClusterHandler)
    * [FindOrEstablishPASESession](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.FindOrEstablishPASESession)
    * [GetConnectedDeviceSync](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetConnectedDeviceSync)
    * [WaitForActive](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.WaitForActive)
    * [GetConnectedDevice](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetConnectedDevice)
    * [ComputeRoundTripTimeout](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.ComputeRoundTripTimeout)
    * [GetRemoteSessionParameters](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetRemoteSessionParameters)
    * [TestOnlySendBatchCommands](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.TestOnlySendBatchCommands)
    * [TestOnlySendCommandTimedRequestFlagWithNoTimedInvoke](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.TestOnlySendCommandTimedRequestFlagWithNoTimedInvoke)
    * [TestOnlyWriteAttributeWithMismatchedTimedRequestField](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.TestOnlyWriteAttributeWithMismatchedTimedRequestField)
    * [SendCommand](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.SendCommand)
    * [SendBatchCommands](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.SendBatchCommands)
    * [SendGroupCommand](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.SendGroupCommand)
    * [WriteAttribute](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.WriteAttribute)
    * [TestOnlyWriteAttributeWithLegacyList](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.TestOnlyWriteAttributeWithLegacyList)
    * [WriteGroupAttribute](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.WriteGroupAttribute)
    * [TestOnlyPrepareToReceiveBdxData](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.TestOnlyPrepareToReceiveBdxData)
    * [TestOnlyPrepareToSendBdxData](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.TestOnlyPrepareToSendBdxData)
    * [Read](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.Read)
    * [ReadAttribute](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.ReadAttribute)
    * [ReadEvent](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.ReadEvent)
    * [SetIpk](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetIpk)
    * [InitGroupTestingData](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.InitGroupTestingData)
    * [SetGroupKeySet](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetGroupKeySet)
    * [SetGroupInfo](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetGroupInfo)
    * [AddGroupEndpoint](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.AddGroupEndpoint)
    * [SetGroupKey](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetGroupKey)
    * [RemoveGroupInfo](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.RemoveGroupInfo)
    * [RemoveKeySet](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.RemoveKeySet)
    * [RemoveGroupKeys](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.RemoveGroupKeys)
    * [CreateManualCode](#matter.ChipDeviceCtrl.ChipDeviceControllerBase.CreateManualCode)
  * [ChipDeviceController](#matter.ChipDeviceCtrl.ChipDeviceController)
    * [Commission](#matter.ChipDeviceCtrl.ChipDeviceController.Commission)
    * [CommissionBleThread](#matter.ChipDeviceCtrl.ChipDeviceController.CommissionBleThread)
    * [CommissionNfcThread](#matter.ChipDeviceCtrl.ChipDeviceController.CommissionNfcThread)
    * [CommissionNfcWiFi](#matter.ChipDeviceCtrl.ChipDeviceController.CommissionNfcWiFi)
    * [CommissionNfcEthernet](#matter.ChipDeviceCtrl.ChipDeviceController.CommissionNfcEthernet)
    * [CommissionBleWiFi](#matter.ChipDeviceCtrl.ChipDeviceController.CommissionBleWiFi)
    * [SetWiFiCredentials](#matter.ChipDeviceCtrl.ChipDeviceController.SetWiFiCredentials)
    * [SetThreadOperationalDataset](#matter.ChipDeviceCtrl.ChipDeviceController.SetThreadOperationalDataset)
    * [ResetCommissioningParameters](#matter.ChipDeviceCtrl.ChipDeviceController.ResetCommissioningParameters)
    * [SetTimeZone](#matter.ChipDeviceCtrl.ChipDeviceController.SetTimeZone)
    * [SetDSTOffset](#matter.ChipDeviceCtrl.ChipDeviceController.SetDSTOffset)
    * [SetTCAcknowledgements](#matter.ChipDeviceCtrl.ChipDeviceController.SetTCAcknowledgements)
    * [SetSkipCommissioningComplete](#matter.ChipDeviceCtrl.ChipDeviceController.SetSkipCommissioningComplete)
    * [SetDefaultNTP](#matter.ChipDeviceCtrl.ChipDeviceController.SetDefaultNTP)
    * [SetTrustedTimeSource](#matter.ChipDeviceCtrl.ChipDeviceController.SetTrustedTimeSource)
    * [SetCheckMatchingFabric](#matter.ChipDeviceCtrl.ChipDeviceController.SetCheckMatchingFabric)
    * [GenerateICDRegistrationParameters](#matter.ChipDeviceCtrl.ChipDeviceController.GenerateICDRegistrationParameters)
    * [EnableICDRegistration](#matter.ChipDeviceCtrl.ChipDeviceController.EnableICDRegistration)
    * [DisableICDRegistration](#matter.ChipDeviceCtrl.ChipDeviceController.DisableICDRegistration)
    * [GetFabricCheckResult](#matter.ChipDeviceCtrl.ChipDeviceController.GetFabricCheckResult)
    * [CommissionOnNetwork](#matter.ChipDeviceCtrl.ChipDeviceController.CommissionOnNetwork)
    * [CommissionThreadMeshcop](#matter.ChipDeviceCtrl.ChipDeviceController.CommissionThreadMeshcop)
    * [CommissionViaProxy](#matter.ChipDeviceCtrl.ChipDeviceController.CommissionViaProxy)
    * [get\_rcac](#matter.ChipDeviceCtrl.ChipDeviceController.get_rcac)
    * [CommissionWithCode](#matter.ChipDeviceCtrl.ChipDeviceController.CommissionWithCode)
    * [NOCChainCallback](#matter.ChipDeviceCtrl.ChipDeviceController.NOCChainCallback)
    * [IssueNOCChain](#matter.ChipDeviceCtrl.ChipDeviceController.IssueNOCChain)
    * [SetDACRevocationSetPath](#matter.ChipDeviceCtrl.ChipDeviceController.SetDACRevocationSetPath)
  * [BareChipDeviceController](#matter.ChipDeviceCtrl.BareChipDeviceController)
    * [\_\_init\_\_](#matter.ChipDeviceCtrl.BareChipDeviceController.__init__)

<a id="matter.ChipDeviceCtrl"></a>

# matter.ChipDeviceCtrl

Chip Device Controller interface

<a id="matter.ChipDeviceCtrl.RegisterOnActiveCallback"></a>

#### RegisterOnActiveCallback

```python
def RegisterOnActiveCallback(scopedNodeId: ScopedNodeId,
                             callback: typing.Callable[[ScopedNodeId], None])
```

Registers a callback when the device with given (fabric index, node id) becomes active.

Does nothing if the callback is already registered.

<a id="matter.ChipDeviceCtrl.UnregisterOnActiveCallback"></a>

#### UnregisterOnActiveCallback

```python
def UnregisterOnActiveCallback(scopedNodeId: ScopedNodeId,
                               callback: typing.Callable[[ScopedNodeId],
                                                         None])
```

Unregisters a callback when the device with given (fabric index, node id) becomes active.

Does nothing if the callback has not been registered.

<a id="matter.ChipDeviceCtrl.WaitForCheckIn"></a>

#### WaitForCheckIn

```python
async def WaitForCheckIn(scopedNodeId: ScopedNodeId, timeoutSeconds: float)
```

Waits for a device becomes active.

**Returns**:

  - A future, completes when the device becomes active.

<a id="matter.ChipDeviceCtrl.CallbackContext"></a>

## CallbackContext

```python
class CallbackContext()
```

A context manager for handling callbacks that are expected to be called exactly once.

The context manager makes sure that no concurrent operations which use the same callback
handlers are executed.

<a id="matter.ChipDeviceCtrl.CommissioningContext"></a>

## CommissioningContext

```python
class CommissioningContext(CallbackContext)
```

A context manager for handling commissioning callbacks that are expected to be called exactly once.

This context also resets commissioning related device controller state.

<a id="matter.ChipDeviceCtrl.CommissionableNode"></a>

## CommissionableNode

```python
class CommissionableNode(discovery.CommissionableNode)
```

<a id="matter.ChipDeviceCtrl.CommissionableNode.Commission"></a>

#### Commission

```python
def Commission(nodeId: int, setupPinCode: int) -> int
```

Commission the device using the device controller discovered this device.

nodeId: The nodeId commissioned to the device
setupPinCode: The setup pin code of the device

**Returns**:

- `int` - Effective Node ID of the device (as defined by the assigned NOC)

<a id="matter.ChipDeviceCtrl.DeviceProxyWrapper"></a>

## DeviceProxyWrapper

```python
class DeviceProxyWrapper()
```

Encapsulates a pointer to OperationalDeviceProxy on the c++ side that needs to be
freed when DeviceProxyWrapper goes out of scope. There is a potential issue where
if this is copied around that a double free will occur, but how this is used today
that is not an issue that needs to be accounted for and it will become very apparent
if that happens.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase"></a>

## ChipDeviceControllerBase

```python
class ChipDeviceControllerBase()
```

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.Shutdown"></a>

#### Shutdown

```python
def Shutdown()
```

Shuts down this controller and reclaims any used resources, including the bound
C++ constructor instance in the SDK.

**Raises**:

- `ChipStackError` - On failure.
  

**Returns**:

  None

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.ShutdownAll"></a>

#### ShutdownAll

```python
def ShutdownAll()
```

Shut down all active controllers and reclaim any used resources.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.CheckIsActive"></a>

#### CheckIsActive

```python
def CheckIsActive()
```

Checks if the device controller is active.

**Raises**:

- `RuntimeError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.IsConnected"></a>

#### IsConnected

```python
def IsConnected()
```

Checks if the device controller is connected.

**Returns**:

- `bool` - True if is connected, False if not connected.
  

**Raises**:

- `RuntimeError` - If '_isActive' is False (from the call to CheckIsActive).

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.ConnectBLE"></a>

#### ConnectBLE

```python
async def ConnectBLE(discriminator: int,
                     setupPinCode: int,
                     nodeId: int,
                     isShortDiscriminator: bool = False) -> int
```

Connect to a BLE device via PASE using the given discriminator and setup pin code.

**Arguments**:

- `discriminator` _int_ - The long discriminator for the DNS-SD advertisement. Valid range: 0-4095.
- `setupPinCode` _int_ - The setup pin code of the device.
- `nodeId` _int_ - The node ID of the device.
- `isShortDiscriminator` _Optional[bool]_ - Optional short discriminator.
  

**Returns**:

- `int` - Effective Node ID of the device (as defined by the assigned NOC).

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.ConnectNFC"></a>

#### ConnectNFC

```python
async def ConnectNFC(discriminator: int, setupPinCode: int,
                     nodeId: int) -> int
```

Connect to a NFC device via PASE using the given discriminator and setup pin code.

**Arguments**:

- `discriminator` _int_ - The long discriminator for the DNS-SD advertisement. Valid range: 0-4095.
- `setupPinCode` _int_ - The setup pin code of the device.
- `nodeId` _int_ - The node ID of the device.
  

**Returns**:

- `int` - Effective Node ID of the device (as defined by the assigned NOC).

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.ContinueCommissioningAfterConnectNetworkRequest"></a>

#### ContinueCommissioningAfterConnectNetworkRequest

```python
async def ContinueCommissioningAfterConnectNetworkRequest(nodeId: int) -> int
```

This method is used in case of NFC-based Commissioning without power.
It instructs the commissioner to proceed to the 2nd commissioning phase on the
operational network, after the device has connected to that network.

**Arguments**:

- `nodeId` _int_ - The node ID of the device (commissionee).
  

**Returns**:

- `int` - Effective Node ID of the device (as defined by the assigned NOC).

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.UnpairDevice"></a>

#### UnpairDevice

```python
async def UnpairDevice(nodeId: int) -> None
```

Unpairs the device with the specified node ID.

**Arguments**:

- `nodeId` _int_ - The node ID of the device.
  

**Returns**:

  None.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.CloseBLEConnection"></a>

#### CloseBLEConnection

```python
def CloseBLEConnection()
```

Closes the BLE connection for the device controller.

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.ExpireSessions"></a>

#### ExpireSessions

```python
def ExpireSessions(nodeId: int)
```

Close all sessions with `nodeId` (if any existed) so that sessions get re-established.

This is needed to properly handle operations that invalidate a node's state, such as
UpdateNOC.

WARNING: ONLY CALL THIS IF YOU UNDERSTAND THE SIDE-EFFECTS

**Arguments**:

- `nodeId` _int_ - The node ID of the device.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.MarkSessionDefunct"></a>

#### MarkSessionDefunct

```python
def MarkSessionDefunct(nodeId: int)
```

Marks a previously active session with the specified node as defunct to temporarily prevent it
from being used with new exchanges to send or receive messages. This should be called when there
is suspicion of a loss-of-sync with the session state on the associated peer, such as evidence
of transport failure.

If messages are received thereafter on this session, the session will be put back into the Active state.

This function should only be called on an active session.
This will NOT detach any existing SessionHolders.

**Arguments**:

- `nodeId` _int_ - The node ID of the device whose session should be marked as defunct.
  

**Raises**:

- `RuntimeError` - If the controller is not active.
- `PyChipError` - If the operation fails.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.StopPairing"></a>

#### StopPairing

```python
def StopPairing(nodeId: int)
```

Stop any in-progress PASE/commissioning session with `nodeId` and release the associated
commissionee device proxy, if any.

Unlike ExpireSessions, this does NOT expire operational (CASE) sessions, so it is safe to
call while an operational session to the node is in use.

This is a best-effort teardown: if no commissionee device is currently being paired, the
underlying call returns CHIP_ERROR_INVALID_DEVICE_DESCRIPTOR, which surfaces here as a
ChipStackError that the caller may choose to ignore.

**Arguments**:

- `nodeId` _int_ - The node ID of the device whose pairing should be stopped.
  

**Raises**:

- `RuntimeError` - If the controller is not active.
- `ChipStackError` - On failure (including when there is no pairing in progress to stop).

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.MarkSessionForEviction"></a>

#### MarkSessionForEviction

```python
def MarkSessionForEviction(nodeId: int)
```

Marks the session with the specified node for eviction. It will first detach all SessionHolders
attached to this session by calling 'OnSessionReleased' on each of them. This will force them
to release their reference to the session. If there are no more references left, the session
will then be de-allocated.

Once marked for eviction, the session SHALL NOT ever become active again.

**Arguments**:

- `nodeId` _int_ - The node ID of the device whose session should be marked for eviction.
  

**Raises**:

- `RuntimeError` - If the controller is not active.
- `PyChipError` - If the operation fails.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.DeleteAllSessionResumptionStorage"></a>

#### DeleteAllSessionResumptionStorage

```python
def DeleteAllSessionResumptionStorage()
```

Remove all session resumption information associated with the fabric index of the controller.

**Raises**:

- `RuntimeError` - If the controller is not active.
- `PyChipError` - If the operation fails.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetLocalMRPConfig"></a>

#### SetLocalMRPConfig

```python
def SetLocalMRPConfig(idle_ms: int, active_ms: int, active_threshold_ms: int)
```

Set the local MRP config. This will be advertised to peers and used by them for message retransmissions.

**Arguments**:

- `idle_ms` _int_ - The idle retransmission interval in milliseconds.
- `active_ms` _int_ - The active retransmission interval in milliseconds.
- `active_threshold_ms` _int_ - The active threshold time in milliseconds.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.ResetLocalMRPConfig"></a>

#### ResetLocalMRPConfig

```python
def ResetLocalMRPConfig()
```

Resets the local MRP config to the default values.

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.EstablishPASESessionBLE"></a>

#### EstablishPASESessionBLE

```python
async def EstablishPASESessionBLE(setupPinCode: int, discriminator: int,
                                  nodeId: int) -> None
```

Establish a PASE session over BLE.

Warning: This method attempts to establish a new PASE session, even if an open session already exists.
For safer session management that reuses existing sessions, see `FindOrEstablishPASESession`.

**Arguments**:

- `discriminator` _int_ - The long discriminator for the DNS-SD advertisement. Valid range: 0-4095.
- `setupPinCode` _int_ - The setup pin code of the device.
- `nodeId` _int_ - The node ID of the device.
  

**Returns**:

  None

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.EstablishPASESessionIP"></a>

#### EstablishPASESessionIP

```python
async def EstablishPASESessionIP(ipaddr: str,
                                 setupPinCode: int,
                                 nodeId: int,
                                 port: int = 0) -> None
```

Establish a PASE session over IP.

Warning: This method attempts to establish a new PASE session, even if an open session already exists.
For safer session management that reuses existing sessions, see `FindOrEstablishPASESession`.

**Arguments**:

- `ipaddr` _str_ - IP address.
- `port` _int_ - IP port to use (default is 0).
- `setupPinCode` _int_ - The setup pin code of the device.
- `nodeId` _int_ - The node ID of the device.
  

**Returns**:

  None

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.EstablishPASESessionThreadMeshcop"></a>

#### EstablishPASESessionThreadMeshcop

```python
async def EstablishPASESessionThreadMeshcop(baAddr: str, setupCode: str,
                                            nodeId: int, baPort: int) -> None
```

Establish a PASE session over Thread MeshCoP.

Warning: This method attempts to establish a new PASE session, even if an open session already exists.
For safer session management that reuses existing sessions, see `FindOrEstablishPASESession`.

**Arguments**:

- `baAddr` _str_ - IP address of BorderAgent.
- `setupCode` _str_ - The setup code of the device.
- `nodeId` _int_ - The node ID of the device.
- `baPort` _int_ - IP port of BorderAgent.
  

**Returns**:

  None

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.EstablishPASESession"></a>

#### EstablishPASESession

```python
async def EstablishPASESession(setUpCode: str, nodeId: int) -> None
```

Establish a PASE session using setUpCode.

Warning: This method attempts to establish a new PASE session, even if an open session already exists.
For safer session management that reuses existing sessions, see `FindOrEstablishPASESession`.

**Arguments**:

- `setUpCode` _str_ - The setup code of the device.
- `nodeId` _int_ - The node ID assigned to the device for the PASE session.
  

**Returns**:

  None

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetTestCommissionerUsed"></a>

#### GetTestCommissionerUsed

```python
def GetTestCommissionerUsed()
```

Get the status of test commissioner in use.

**Returns**:

- `bool` - True if the test commissioner is in use, False if not.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetTestCommissionerSimulateFailureOnStage"></a>

#### SetTestCommissionerSimulateFailureOnStage

```python
def SetTestCommissionerSimulateFailureOnStage(stage: int)
```

Simulates a failure on a specific stage of the test commissioner.

**Arguments**:

- `stage` _int_ - The commissioning stage where failure will be simulated.
  This corresponds to the enum `CommissioningStage` (e.g. kError, kSecurePairing, etc.). For full details
  ref https://github.com/project-chip/connectedhomeip/blob/master/src/controller/CommissioningDelegate.h
  

**Returns**:

- `bool` - True if the failure simulate success, False if not.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetTestCommissionerSimulateFailureOnReport"></a>

#### SetTestCommissionerSimulateFailureOnReport

```python
def SetTestCommissionerSimulateFailureOnReport(stage: int)
```

Simulates a failure on report of the test commissioner.

**Arguments**:

- `stage` _int_ - The commissioning stage where failure will be simulated.
  This corresponds to the enum `CommissioningStage` (e.g. kError, kSecurePairing, etc.). For full details
  ref https://github.com/project-chip/connectedhomeip/blob/master/src/controller/CommissioningDelegate.h
  

**Returns**:

- `bool` - True if the failure simulate success, False if not.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetTestCommissionerPrematureCompleteAfter"></a>

#### SetTestCommissionerPrematureCompleteAfter

```python
def SetTestCommissionerPrematureCompleteAfter(stage: int)
```

Premature complete of the test commissioner.

**Arguments**:

- `stage` _int_ - The commissioning stage after a premature completion is simulated.
  This corresponds to the enum `CommissioningStage` (e.g. kError, kSecurePairing, etc.). For full details
  ref https://github.com/project-chip/connectedhomeip/blob/master/src/controller/CommissioningDelegate.h
  

**Returns**:

- `bool` - True if the premature complete success, False if not.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.CheckTestCommissionerCallbacks"></a>

#### CheckTestCommissionerCallbacks

```python
def CheckTestCommissionerCallbacks()
```

Check the test commissioner callbacks.

**Returns**:

- `bool` - True if the test commissioner callbacks success, False if not.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.CheckStageSuccessful"></a>

#### CheckStageSuccessful

```python
def CheckStageSuccessful(stage: int)
```

Check the test commissioner stage success.

**Arguments**:

- `stage` _int_ - The commissioning to simulate.
  

**Returns**:

- `bool` - True if test commissioner stage success, False if not.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.CheckTestCommissionerPaseConnection"></a>

#### CheckTestCommissionerPaseConnection

```python
def CheckTestCommissionerPaseConnection(nodeId: int)
```

Check the test commissioner Pase connection success.

**Arguments**:

- `nodeId` _int_ - The node ID of the device.
  

**Returns**:

- `bool` - True if test commissioner Pase connection success, False if not.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.ResolveNode"></a>

#### ResolveNode

```python
def ResolveNode(nodeId: int)
```

Resolve node ID.

**Arguments**:

- `nodeId` _int_ - The node ID of the device.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetAddressAndPort"></a>

#### GetAddressAndPort

```python
def GetAddressAndPort(nodeId: int)
```

Get the address and port.

**Arguments**:

- `nodeId` _int_ - The node ID of the device.
  

**Returns**:

- `tuple` - The address and port if no error occurs or None on failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetLastThreadMeshcopDiscoveryDiagnostic"></a>

#### GetLastThreadMeshcopDiscoveryDiagnostic

```python
def GetLastThreadMeshcopDiscoveryDiagnostic() -> dict[str, typing.Any]
```

Get diagnostic data captured during the most recent Thread MeshCoP discovery.

**Returns**:

- `dict` - Parsed JSON diagnostic data from the native Thread MeshCoP proxy.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.DiscoverCommissionableNodes"></a>

#### DiscoverCommissionableNodes

```python
async def DiscoverCommissionableNodes(
    filterType: discovery.FilterType = discovery.FilterType.NONE,
    filter: typing.Any = None,
    stopOnFirst: bool = False,
    timeoutSecond: int = 5
) -> None | CommissionableNode | list[CommissionableNode]
```

Discover commissionable nodes via DNS-SD with specified filters.
Supported filters are:

discovery.FilterType.NONE
discovery.FilterType.SHORT_DISCRIMINATOR
discovery.FilterType.LONG_DISCRIMINATOR
discovery.FilterType.VENDOR_ID
discovery.FilterType.DEVICE_TYPE
discovery.FilterType.COMMISSIONING_MODE
discovery.FilterType.INSTANCE_NAME
discovery.FilterType.COMMISSIONER
discovery.FilterType.COMPRESSED_FABRIC_ID

This function will always return a list of CommissionableDevice. When stopOnFirst is set,
this function will return when at least one device is discovered or on timeout.

**Returns**:

- `list` - A list of discovered devices.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetDiscoveredDevices"></a>

#### GetDiscoveredDevices

```python
async def GetDiscoveredDevices()
```

Get the discovered devices.

**Returns**:

- `list` - A list of discovered devices.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetIPForDiscoveredDevice"></a>

#### GetIPForDiscoveredDevice

```python
def GetIPForDiscoveredDevice(idx, addrStr, length)
```

Get the IP address for a discovered device.

**Arguments**:

- `idx` _int_ - Index of the discovered device.
- `addrStr` _str_ - Address of the device.
- `length` _int_ - Length of the address.
  

**Returns**:

- `bool` - True if IP for discovered device success, False if not.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.OpenCommissioningWindow"></a>

#### OpenCommissioningWindow

```python
async def OpenCommissioningWindow(
        nodeId: int,
        timeout: int,
        iteration: int,
        discriminator: int,
        option: CommissioningWindowPasscode,
        setupPinCode: int = 0) -> CommissioningParameters
```

Opens a commissioning window on the device with the given node ID.

**Arguments**:

- `nodeId` _int_ - The node ID of the device.
- `timeout` _int_ - Command timeout
- `iteration` _int_ - The PAKE iteration count associated with the PAKE Passcode ID and ephemeral
  PAKE passcode verifier to be used for this commissioning. Valid range: 1000 - 100000
  Ignored if option == 0
- `discriminator` _int_ - The long discriminator for the DNS-SD advertisement. Valid range: 0-4095
  Ignored if option == 0
  option (int):
  0 = kOriginalSetupCode
  1 = kTokenWithRandomPIN
  2 = kTokenWithProvidedPIN
- `setupPinCode` _int_ - The setup PIN code to use. Ignored if option != 2
  

**Returns**:

  CommissioningParameters

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.OpenJointCommissioningWindow"></a>

#### OpenJointCommissioningWindow

```python
async def OpenJointCommissioningWindow(
        nodeId: int, endpointId: int, timeout: int, iteration: int,
        discriminator: int) -> CommissioningParameters
```

Opens a joint commissioning window on the device with the given node ID.

**Arguments**:

- `nodeId` _int_ - The node ID of the device.
- `timeout` _int_ - Command timeout
- `iteration` _int_ - The PAKE iteration count associated with the PAKE Passcode ID and ephemeral
  PAKE passcode verifier to be used for this commissioning. Valid range: 1000 - 100000
- `discriminator` _int_ - The long discriminator for the DNS-SD advertisement. Valid range: 0-4095
  

**Returns**:

  CommissioningParameters

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetCompressedFabricId"></a>

#### GetCompressedFabricId

```python
def GetCompressedFabricId()
```

Get compressed fabric Id.

**Returns**:

- `int` - The compressed fabric ID as a 64-bit integer.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetFabricIdInternal"></a>

#### GetFabricIdInternal

```python
def GetFabricIdInternal() -> int
```

Get the fabric ID from the object. Only used to validate cached value from property.

**Returns**:

- `int` - The raw fabric ID as a 64-bit integer.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetFabricIndexInternal"></a>

#### GetFabricIndexInternal

```python
def GetFabricIndexInternal() -> int
```

Get the fabric index from the object. Only used to validate cached value from property.

**Returns**:

- `int` - fabric index in local fabric table associated with this controller.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetNodeIdInternal"></a>

#### GetNodeIdInternal

```python
def GetNodeIdInternal() -> int
```

Get the node ID from the object. Only used to validate cached value from property.

**Returns**:

- `int` - The Node ID as a 64 bit integer.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetRootPublicKeyBytesInternal"></a>

#### GetRootPublicKeyBytesInternal

```python
def GetRootPublicKeyBytesInternal() -> bytes
```

Get the root public key associated with our fabric.

**Returns**:

- `bytes` - The root public key raw bytes in uncompressed point form.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetClusterHandler"></a>

#### GetClusterHandler

```python
def GetClusterHandler()
```

Get cluster handler

**Returns**:

- `ChipClusters` - An instance of the ChipClusters class.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.FindOrEstablishPASESession"></a>

#### FindOrEstablishPASESession

```python
async def FindOrEstablishPASESession(
    setupCode: str,
    nodeId: int,
    timeoutMs: int | None = None,
    threadMeshCoPConfig: tuple[str, int] | None = None
) -> DeviceProxyWrapper | None
```

Find or establish a PASE session.

**Arguments**:

- `setUpCode` _str_ - The setup code of the device.
- `nodeId` _int_ - The node ID of the device.
- `timeoutMs` _Optional[int]_ - Optional timeout in milliseconds.
- `threadMeshCoPConfig` _Optional[tuple[str, int]]_ - Optional Border Agent host and port for Thread MeshCoP PASE.
  

**Returns**:

  DeviceProxyWrapper on success, if not is None.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetConnectedDeviceSync"></a>

#### GetConnectedDeviceSync

```python
def GetConnectedDeviceSync(
        nodeId: int,
        allowPASE=True,
        timeoutMs: int | None = None,
        payloadCapability: int = TransportPayloadCapability.MRP_PAYLOAD)
```

Gets an OperationalDeviceProxy or CommissioneeDeviceProxy for the specified Node.

**Arguments**:

- `nodeId` _int_ - Target's Node ID
- `allowPASE` _bool_ - Get a device proxy of a device being commissioned.
- `timeoutMs` _Optional[int]_ - Timeout for a timed invoke request. Omit or set to 'None' to indicate a non-timed request.
  

**Returns**:

  DeviceProxyWrapper on success.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.WaitForActive"></a>

#### WaitForActive

```python
async def WaitForActive(nodeId: int,
                        *,
                        timeoutSeconds=30.0,
                        stayActiveDurationMs=30000)
```

Waits a LIT ICD device to become active. Will send a StayActive command to the device on active to allow human operations.

**Arguments**:

- `nodeId` - Node ID of the LID ICD.
- `stayActiveDurationMs` - The duration in the StayActive command, in milliseconds.
  

**Returns**:

  StayActiveResponse on success

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetConnectedDevice"></a>

#### GetConnectedDevice

```python
async def GetConnectedDevice(
        nodeId: int,
        allowPASE: bool = True,
        timeoutMs: int | None = None,
        payloadCapability: int = TransportPayloadCapability.MRP_PAYLOAD)
```

Gets an OperationalDeviceProxy or CommissioneeDeviceProxy for the specified Node.

**Arguments**:

- `nodeId` _int_ - Target's Node ID.
- `allowPASE` _bool_ - Get a device proxy of a device being commissioned.
- `timeoutMs` _Optional[int]_ - Timeout for a timed invoke request. Omit or set to 'None' to indicate a non-timed request.
  

**Returns**:

  DeviceProxyWrapper on success.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.ComputeRoundTripTimeout"></a>

#### ComputeRoundTripTimeout

```python
def ComputeRoundTripTimeout(nodeId: int,
                            upperLayerProcessingTimeoutMs: int = 0)
```

Returns a computed timeout value based on the round-trip time it takes for the peer at the other end of the session to
receive a message, process it and send it back. This is computed based on the session type, the type of transport,
sleepy characteristics of the target and a caller-provided value for the time it takes to process a message
at the upper layer on the target For group sessions.

This will result in a session being established if one wasn't already.

**Returns**:

- `int` - The computed timeout value in milliseconds, representing the round-trip time.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.GetRemoteSessionParameters"></a>

#### GetRemoteSessionParameters

```python
def GetRemoteSessionParameters(nodeId: int) -> SessionParameters | None
```

Returns the SessionParameters of reported by the remote node associated with `nodeId`.
If there is some error in getting SessionParameters None is returned.

This will result in a session being established if one wasn't already established.

**Returns**:

- `Optional[SessionParameters]` - The session parameters.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.TestOnlySendBatchCommands"></a>

#### TestOnlySendBatchCommands

```python
async def TestOnlySendBatchCommands(
        nodeId: int,
        commands: list[ClusterCommand.InvokeRequestInfo],
        timedRequestTimeoutMs: int | None = None,
        interactionTimeoutMs: int | None = None,
        busyWaitMs: int | None = None,
        suppressResponse: bool = False,
        remoteMaxPathsPerInvoke: int | None = None,
        suppressTimedRequestMessage: bool = False,
        commandRefsOverride: list[int] | None = None,
        delayReportData: ClusterCommand.DelayReportData | None = None)
```

Please see SendBatchCommands for description.
TestOnly overridable arguments:
remoteMaxPathsPerInvoke: Overrides the number of batch commands we think can be sent to remote node.
suppressTimedRequestMessage: When set to true, we suppress sending Timed Request Message.
commandRefsOverride: List of commandRefs to use for each command with the same index in `commands`.

**Returns**:

  TestOnlyBatchCommandResponse or None

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.TestOnlySendCommandTimedRequestFlagWithNoTimedInvoke"></a>

#### TestOnlySendCommandTimedRequestFlagWithNoTimedInvoke

```python
async def TestOnlySendCommandTimedRequestFlagWithNoTimedInvoke(
        nodeId: int,
        endpoint: int,
        payload: ClusterObjects.ClusterCommand,
        responseType=None)
```

Please see SendCommand for description.

**Returns**:

  Command response. The type of the response is defined by the command.
  

**Raises**:

  InteractionModelError on error

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.TestOnlyWriteAttributeWithMismatchedTimedRequestField"></a>

#### TestOnlyWriteAttributeWithMismatchedTimedRequestField

```python
async def TestOnlyWriteAttributeWithMismatchedTimedRequestField(
        nodeid: int,
        attributes: list[tuple[int, ClusterObjects.ClusterAttributeDescriptor]
                         | tuple[int,
                                 ClusterObjects.ClusterAttributeDescriptor,
                                 int]],
        timedRequestTimeoutMs: int,
        timedRequestFieldValue: bool,
        interactionTimeoutMs: int | None = None,
        busyWaitMs: int | None = None,
        payloadCapability: int = TransportPayloadCapability.MRP_PAYLOAD)
```

ONLY TO BE USED FOR TEST: Write attributes with decoupled Timed Request action and TimedRequest field.
This allows testing TIMED_REQUEST_MISMATCH scenarios:
- timedRequestTimeoutMs=0, timedRequestFieldValue=True: No action, but field=true (MISMATCH)
- timedRequestTimeoutMs>0, timedRequestFieldValue=False: Action sent, but field=false (MISMATCH)

Please see WriteAttribute for description of common parameters.

Additional parameters:
timedRequestTimeoutMs: Timeout for the Timed Request action (0 means no action)
timedRequestFieldValue: Value of the TimedRequest field in WriteRequest

**Returns**:

  [AttributeStatus] (list - one for each path).
  

**Raises**:

  InteractionModelError on error (expected: TIMED_REQUEST_MISMATCH)

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.SendCommand"></a>

#### SendCommand

```python
async def SendCommand(
        nodeId: int,
        endpoint: int,
        payload: ClusterObjects.ClusterCommand,
        responseType=None,
        timedRequestTimeoutMs: int | None = None,
        interactionTimeoutMs: int | None = None,
        busyWaitMs: int | None = None,
        suppressResponse: bool = False,
        payloadCapability: int = TransportPayloadCapability.MRP_PAYLOAD,
        delayReportData: ClusterCommand.DelayReportData | None = None)
```

Send a cluster-object encapsulated command to a node and get returned a future that can be awaited upon to receive
the response. If a valid responseType is passed in, that will be used to de-serialize the object. If not,
the type will be automatically deduced from the metadata received over the wire.

timedWriteTimeoutMs: Timeout for a timed invoke request. Omit or set to 'None' to indicate a non-timed request.
interactionTimeoutMs: Overall timeout for the interaction. Omit or set to 'None' to have the SDK automatically compute the
right timeout value based on transport characteristics as well as the responsiveness of the target.
delayReportData: Optional DelayReportData specifying min delay and jitter window for report suppression during invoke.

**Returns**:

  command response or None. The type of the response is defined by the command.
  

**Raises**:

  InteractionModelError on error

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.SendBatchCommands"></a>

#### SendBatchCommands

```python
async def SendBatchCommands(
        nodeId: int,
        commands: list[ClusterCommand.InvokeRequestInfo],
        timedRequestTimeoutMs: int | None = None,
        interactionTimeoutMs: int | None = None,
        busyWaitMs: int | None = None,
        suppressResponse: bool = False,
        payloadCapability: int = TransportPayloadCapability.MRP_PAYLOAD,
        delayReportData: ClusterCommand.DelayReportData | None = None)
```

Send a batch of cluster-object encapsulated commands to a node and get returned a future that can be awaited upon to receive
the responses. If a valid responseType is passed in, that will be used to de-serialize the object. If not,
the type will be automatically deduced from the metadata received over the wire.

nodeId: Target's Node ID
commands: A list of InvokeRequestInfo containing the commands to invoke.
timedWriteTimeoutMs: Timeout for a timed invoke request. Omit or set to 'None' to indicate a non-timed request.
interactionTimeoutMs: Overall timeout for the interaction. Omit or set to 'None' to have the SDK automatically compute the
right timeout value based on transport characteristics as well as the responsiveness of the target.
busyWaitMs: How long to wait in ms after sending command to device before performing any other operations.
suppressResponse: Do not send a response to this action
delayReportData: Optional DelayReportData specifying min delay and jitter window for report suppression during invoke.

**Returns**:

  - None if suppressResponse is True. Otherwise, a list of command responses in the same order as what was given in `commands`. The type of the response is defined by the command.
  - A value of `None` indicates success.
  - If only a single command fails, for example with `UNSUPPORTED_COMMAND`, the corresponding index associated with the command will,
  contain `interaction_model.Status.UnsupportedCommand`.
  - If a command is not responded to by server, command will contain `interaction_model.Status.NoCommandResponse`

**Raises**:

  - InteractionModelError if error with sending of InvokeRequestMessage fails as a whole.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.SendGroupCommand"></a>

#### SendGroupCommand

```python
def SendGroupCommand(groupid: int,
                     payload: ClusterObjects.ClusterCommand,
                     busyWaitMs: int | None = None)
```

Send a group cluster-object encapsulated command to a group_id and get returned a future
that can be awaited upon to get confirmation command was sent.

**Returns**:

- `None` - responses are not sent to group commands.
  

**Raises**:

  InteractionModelError on error.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.WriteAttribute"></a>

#### WriteAttribute

```python
async def WriteAttribute(
        nodeId: int,
        attributes: list[tuple[int, ClusterObjects.ClusterAttributeDescriptor]
                         | tuple[int,
                                 ClusterObjects.ClusterAttributeDescriptor,
                                 int]],
        timedRequestTimeoutMs: int | None = None,
        interactionTimeoutMs: int | None = None,
        busyWaitMs: int | None = None,
        payloadCapability: int = TransportPayloadCapability.MRP_PAYLOAD,
        suppressResponse: bool = False)
```

Write a list of attributes on a target node.

nodeId: Target's Node ID
timedWriteTimeoutMs: Timeout for a timed write request. Omit or set to 'None' to indicate a non-timed request.
attributes: A list of tuples of type (endpoint, cluster-object):
interactionTimeoutMs: Overall timeout for the interaction. Omit or set to 'None' to have the SDK automatically compute the
right timeout value based on transport characteristics as well as the responsiveness of the target.
suppressResponse: Do not send a response to this action
E.g
(1, Clusters.UnitTesting.Attributes.XYZAttribute('hello')) -- Write 'hello'
to the XYZ attribute on the test cluster to endpoint 1

**Returns**:

  [AttributeStatus] or None (list - one for each path, or None when suppressResponse is True).
  

**Raises**:

  InteractionModelError on error.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.TestOnlyWriteAttributeWithLegacyList"></a>

#### TestOnlyWriteAttributeWithLegacyList

```python
async def TestOnlyWriteAttributeWithLegacyList(
        nodeId: int,
        attributes: list[tuple[int, ClusterObjects.ClusterAttributeDescriptor]
                         | tuple[int,
                                 ClusterObjects.ClusterAttributeDescriptor,
                                 int]],
        timedRequestTimeoutMs: int | None = None,
        interactionTimeoutMs: int | None = None,
        busyWaitMs: int | None = None,
        payloadCapability: int = TransportPayloadCapability.MRP_PAYLOAD)
```

Please see WriteAttribute for description.
This is a test-only wrapper for _WriteAttribute that sets forceLegacyListEncoding to True.

The purpose of this method is to write attributes using the legacy encoding format for list data types, to ensure that end devices support legacy WriteClients.


**Returns**:

  [AttributeStatus] (list - one for each path).
  

**Raises**:

  InteractionModelError on error.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.WriteGroupAttribute"></a>

#### WriteGroupAttribute

```python
def WriteGroupAttribute(
        groupid: int,
        attributes: list[tuple[ClusterObjects.ClusterAttributeDescriptor,
                               int]],
        busyWaitMs: int | None = None)
```

Write a list of attributes on a target group.

groupid: Group ID to send write attribute to.
attributes: A list of tuples of type (cluster-object, data-version). The data-version can be omitted.

E.g
(Clusters.UnitTesting.Attributes.XYZAttribute('hello'), 1) -- Group Write 'hello' with data version 1.

**Returns**:

  list = An empty list
  

**Raises**:

  InteractionModelError on error.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.TestOnlyPrepareToReceiveBdxData"></a>

#### TestOnlyPrepareToReceiveBdxData

```python
def TestOnlyPrepareToReceiveBdxData(
        max_block_size: int | None = None) -> asyncio.Future
```

Sets up the system to expect a node to initiate a BDX transfer. The transfer will send data here.

If no BDX transfer is initiated, the caller must cancel the returned future to avoid interfering with other BDX transfers.
For example, the Diagnostic Logs clusters won't start a BDX transfer when the log is small so the future must be cancelled to allow later
attempts to retrieve logs to succeed.

If max_block_size is provided (1..65535), it overrides the controller's default cap.

**Returns**:

  a future that will yield a BdxTransfer with the init message from the transfer.
  

**Raises**:

  InteractionModelError on error.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.TestOnlyPrepareToSendBdxData"></a>

#### TestOnlyPrepareToSendBdxData

```python
def TestOnlyPrepareToSendBdxData(data: bytes) -> asyncio.Future
```

Sets up the system to expect a node to initiate a BDX transfer. The transfer will send data to the node.

If no BDX transfer is initiated, the caller must cancel the returned future to avoid interfering with other BDX transfers.

**Returns**:

  A future that will yield a BdxTransfer with the init message from the transfer.
  

**Raises**:

  InteractionModelError on error.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.Read"></a>

#### Read

```python
async def Read(
        nodeId: int,
        attributes:
    list[None  # Empty tuple, all wildcard
         | tuple[int]  # Endpoint
         | tuple[type[ClusterObjects.
                      Cluster]]  # Wildcard endpoint, Cluster id present
         | tuple[type[
             ClusterObjects.
             ClusterAttributeDescriptor]]  # Wildcard endpoint, Cluster + Attribute present
         | tuple[int, type[ClusterObjects.Cluster]]  # Wildcard attribute id
         | tuple[int, type[ClusterObjects.
                           ClusterAttributeDescriptor]]  # Concrete path
         | ClusterAttribute.AttributePath  # Directly specified attribute path
         ] | None = None,
        dataVersionFilters: list[tuple[int, type[ClusterObjects.Cluster], int]]
    | None = None,
        events: list[None  # Empty tuple, all wildcard
                     | tuple[str, int]  # all wildcard with urgency set
                     | tuple[int, int]  # Endpoint
                     | tuple[type[ClusterObjects.Cluster],
                             int]  # Wildcard endpoint, Cluster id present
                     | tuple[type[ClusterObjects.ClusterEvent],
                             int]  # Wildcard endpoint, Cluster + Event present
                     | tuple[int, type[ClusterObjects.Cluster],
                             int]  # Wildcard event id
                     | tuple[int, type[ClusterObjects.ClusterEvent],
                             int]  # Concrete path
                     ] | None = None,
        eventNumberFilter: int | None = None,
        returnClusterObject: bool = False,
        reportInterval: tuple[int, int] | None = None,
        fabricFiltered: bool = True,
        keepSubscriptions: bool = False,
        autoResubscribe: bool = True,
        payloadCapability: int = TransportPayloadCapability.MRP_PAYLOAD)
```

Read a list of attributes and/or events from a target node

nodeId: Target's Node ID
attributes: A list of tuples of varying types depending on the type of read being requested:
(endpoint, Clusters.ClusterA.AttributeA):   Endpoint = specific,    Cluster = specific,   Attribute = specific
(endpoint, Clusters.ClusterA):              Endpoint = specific,    Cluster = specific,   Attribute = *
(Clusters.ClusterA.AttributeA):             Endpoint = *,           Cluster = specific,   Attribute = specific
endpoint:                                   Endpoint = specific,    Cluster = *,          Attribute = *
Clusters.ClusterA:                          Endpoint = *,           Cluster = specific,   Attribute = *
'*' or ():                                  Endpoint = *,           Cluster = *,          Attribute = *

The cluster and attributes specified above are to be selected from the generated cluster objects.

e.g.
ReadAttribute(1, [ 1 ] ) -- case 4 above.
ReadAttribute(1, [ Clusters.BasicInformation ] ) -- case 5 above.
ReadAttribute(1, [ (1, Clusters.BasicInformation.Attributes.Location ] ) -- case 1 above.

An AttributePath can also be specified directly by [matter.cluster.Attribute.AttributePath(...)]

dataVersionFilters: A list of tuples of (endpoint, cluster, data version).

events: A list of tuples of varying types depending on the type of read being requested:
(endpoint, Clusters.ClusterA.EventA, urgent):       Endpoint = specific,
Cluster = specific,   Event = specific, Urgent = True/False
(endpoint, Clusters.ClusterA, urgent):              Endpoint = specific,
Cluster = specific,   Event = *, Urgent = True/False
(Clusters.ClusterA.EventA, urgent):                 Endpoint = *,
Cluster = specific,   Event = specific, Urgent = True/False
endpoint:                                   Endpoint = specific,    Cluster = *,          Event = *, Urgent = True/False
Clusters.ClusterA:                          Endpoint = *,          Cluster = specific,    Event = *, Urgent = True/False
'*' or ():                                  Endpoint = *,          Cluster = *,          Event = *, Urgent = True/False

eventNumberFilter: Optional minimum event number filter.

returnClusterObject: This returns the data as consolidated cluster objects, with all attributes for a cluster inside
a single cluster-wide cluster object.

reportInterval: A tuple of two int-s for (MinIntervalFloor, MaxIntervalCeiling). Used by establishing subscriptions.
When not provided, a read request will be sent.
fabricFiltered: If True (default), the read/subscribe is fabric-filtered and will only see things associated with the fabric
of the reader/subscriber. Relevant for attributes with fabric-scoped data.
keepSubscriptions: Keep existing subscriptions. If set to False, existing subscriptions with this node will get cancelled
and a new one gets setup.
autoResubscribe: Automatically resubscribe to the subscription if subscription is lost. The automatic re-subscription only
applies if the subscription establishes on first try. If the first subscription establishment attempt fails the function
returns right away.

**Returns**:

  - AsyncReadTransaction.ReadResponse. Please see ReadAttribute and ReadEvent for examples of how to access data.
  

**Raises**:

  - InteractionModelError (matter.interaction_model) on error

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.ReadAttribute"></a>

#### ReadAttribute

```python
async def ReadAttribute(
        nodeId: int,
        attributes:
    list[None  # Empty tuple, all wildcard
         | tuple[int]  # Endpoint
         | tuple[type[ClusterObjects.
                      Cluster]]  # Wildcard endpoint, Cluster id present
         | tuple[type[
             ClusterObjects.
             ClusterAttributeDescriptor]]  # Wildcard endpoint, Cluster + Attribute present
         | tuple[int, type[ClusterObjects.Cluster]]  # Wildcard attribute id
         | tuple[int, type[ClusterObjects.
                           ClusterAttributeDescriptor]]  # Concrete path
         | ClusterAttribute.AttributePath  # Directly specified attribute path
         ] | None,
        dataVersionFilters: list[tuple[int, type[ClusterObjects.Cluster], int]]
    | None = None,
        returnClusterObject: bool = False,
        reportInterval: tuple[int, int] | None = None,
        fabricFiltered: bool = True,
        keepSubscriptions: bool = False,
        autoResubscribe: bool = True,
        payloadCapability: int = TransportPayloadCapability.MRP_PAYLOAD)
```

Read a list of attributes from a target node, this is a wrapper of DeviceController.Read()

nodeId: Target's Node ID
attributes: A list of tuples of varying types depending on the type of read being requested:
(endpoint, Clusters.ClusterA.AttributeA):   Endpoint = specific,    Cluster = specific,   Attribute = specific
(endpoint, Clusters.ClusterA):              Endpoint = specific,    Cluster = specific,   Attribute = *
(Clusters.ClusterA.AttributeA):             Endpoint = *,           Cluster = specific,   Attribute = specific
endpoint:                                   Endpoint = specific,    Cluster = *,          Attribute = *
Clusters.ClusterA:                          Endpoint = *,           Cluster = specific,   Attribute = *
'*' or ():                                  Endpoint = *,           Cluster = *,          Attribute = *

The cluster and attributes specified above are to be selected from the generated cluster objects.

e.g.
ReadAttribute(1, [ 1 ] ) -- case 4 above.
ReadAttribute(1, [ Clusters.BasicInformation ] ) -- case 5 above.
ReadAttribute(1, [ (1, Clusters.BasicInformation.Attributes.Location ] ) -- case 1 above.

An AttributePath can also be specified directly by [matter.cluster.Attribute.AttributePath(...)]

returnClusterObject: This returns the data as consolidated cluster objects, with all attributes for a cluster inside
a single cluster-wide cluster object.

reportInterval: A tuple of two int-s for (MinIntervalFloor, MaxIntervalCeiling). Used by establishing subscriptions.
When not provided, a read request will be sent.
fabricFiltered: If True (default), the read/subscribe is fabric-filtered and will only see things associated with the fabric
of the reader/subscriber. Relevant for attributes with fabric-scoped data.
keepSubscriptions: Keep existing subscriptions. If set to False, existing subscriptions with this node will get cancelled
and a new one gets setup.
autoResubscribe: Automatically resubscribe to the subscription if subscription is lost. The automatic re-subscription only
applies if the subscription establishes on first try. If the first subscription establishment attempt fails the function
returns right away.

**Returns**:

  - subscription request: ClusterAttribute.SubscriptionTransaction
  To get notified on attribute change use SetAttributeUpdateCallback on the returned
  SubscriptionTransaction. This is used to set a callback function, which is a callable of
  type Callable[[TypedAttributePath, SubscriptionTransaction], None]
  Get the attribute value from the change path using GetAttribute on the SubscriptionTransaction
  You can await changes in the main loop using a trigger mechanism from the callback.
  ex. queue.SimpleQueue
  
  - read request: AsyncReadTransaction.ReadResponse.attributes.
  This is of type AttributeCache.attributeCache (Attribute.py),
  which is a dict mapping endpoints to a list of Cluster (ClusterObjects.py) classes
  (dict[int, List[Cluster]])
  Access as returned_object[endpoint_id][<Cluster class>][<Attribute class>]
  Ex. To access the OnTime attribute from the OnOff cluster on endpoint 1
  returned_object[1][Clusters.OnOff][Clusters.OnOff.Attributes.OnTime]
  

**Raises**:

  - InteractionModelError (matter.interaction_model) on error

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.ReadEvent"></a>

#### ReadEvent

```python
async def ReadEvent(
        nodeId: int,
        events: list[None  # Empty tuple, all wildcard
                     | tuple[str, int]  # all wildcard with urgency set
                     | tuple[int, int]  # Endpoint
                     | tuple[type[ClusterObjects.Cluster],
                             int]  # Wildcard endpoint, Cluster id present
                     | tuple[type[ClusterObjects.ClusterEvent],
                             int]  # Wildcard endpoint, Cluster + Event present
                     | tuple[int, type[ClusterObjects.Cluster],
                             int]  # Wildcard event id
                     | tuple[int, type[ClusterObjects.ClusterEvent],
                             int]  # Concrete path
                     ],
        eventNumberFilter: int | None = None,
        fabricFiltered: bool = True,
        reportInterval: tuple[int, int] | None = None,
        keepSubscriptions: bool = False,
        autoResubscribe: bool = True,
        payloadCapability: int = TransportPayloadCapability.MRP_PAYLOAD)
```

Read a list of events from a target node, this is a wrapper of DeviceController.Read()

nodeId: Target's Node ID
events: A list of tuples of varying types depending on the type of read being requested:
(endpoint, Clusters.ClusterA.EventA, urgent):       Endpoint = specific,
Cluster = specific,   Event = specific, Urgent = True/False
(endpoint, Clusters.ClusterA, urgent):              Endpoint = specific,
Cluster = specific,   Event = *, Urgent = True/False
(Clusters.ClusterA.EventA, urgent):                 Endpoint = *,
Cluster = specific,   Event = specific, Urgent = True/False
endpoint:                                   Endpoint = specific,    Cluster = *,          Event = *, Urgent = True/False
Clusters.ClusterA:                          Endpoint = *,          Cluster = specific,    Event = *, Urgent = True/False
'*' or ():                                  Endpoint = *,          Cluster = *,          Event = *, Urgent = True/False

The cluster and events specified above are to be selected from the generated cluster objects.

e.g.
ReadEvent(1, [ 1 ] ) -- case 4 above.
ReadEvent(1, [ Clusters.BasicInformation ] ) -- case 5 above.
ReadEvent(1, [ (1, Clusters.BasicInformation.Events.Location ] ) -- case 1 above.

eventNumberFilter: Optional minimum event number filter.
reportInterval: A tuple of two int-s for (MinIntervalFloor, MaxIntervalCeiling). Used by establishing subscriptions.
When not provided, a read request will be sent.
keepSubscriptions: Keep existing subscriptions. If set to False, existing subscriptions with this node will get cancelled
and a new one gets setup.
autoResubscribe: Automatically resubscribe to the subscription if subscription is lost. The automatic re-subscription only
applies if the subscription establishes on first try. If the first subscription establishment attempt fails the function
returns right away.

**Returns**:

  - subscription request: ClusterAttribute.SubscriptionTransaction
  To get notified on event subscriptions, use the SetEventUpdateCallback function on the
  returned  SubscriptionTransaction. This is a callable of type
  Callable[[EventReadResult, SubscriptionTransaction], None]
  You can await events using a trigger mechanism in the callback. ex. queue.SimpleQueue
  
  - read request: AsyncReadTransaction.ReadResponse.events.
  This is a List[ClusterEvent].
  

**Raises**:

  - InteractionModelError (matter.interaction_model) on error

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetIpk"></a>

#### SetIpk

```python
def SetIpk(ipk: bytes)
```

Sets the Identity Protection Key (IPK) for the device controller.

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.InitGroupTestingData"></a>

#### InitGroupTestingData

```python
def InitGroupTestingData()
```

Populates the Device Controller's GroupDataProvider with known test group info and keys.

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetGroupKeySet"></a>

#### SetGroupKeySet

```python
def SetGroupKeySet(keyset_id: int,
                   policy: int,
                   num_keys: int,
                   epoch_key0: bytes,
                   epoch_start_time0: int,
                   epoch_key1: bytes | None = None,
                   epoch_start_time1: int = 0,
                   epoch_key2: bytes | None = None,
                   epoch_start_time2: int = 0)
```

Writes a GroupKeySet into the controller's GroupDataProvider for this fabric.

**Arguments**:

- `keyset_id` - Key set identifier.
- `policy` - Security policy (0 = TrustFirst, 1 = CacheAndSync).
- `num_keys` - Number of epoch keys (1-3).
- `epoch_key0` - First epoch key (16 bytes).
- `epoch_start_time0` - Start time for first epoch key (microseconds since Matter epoch).
- `epoch_key1` - Second epoch key (16 bytes), or None if unused.
- `epoch_start_time1` - Start time for second epoch key.
- `epoch_key2` - Third epoch key (16 bytes), or None if unused.
- `epoch_start_time2` - Start time for third epoch key.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetGroupInfo"></a>

#### SetGroupInfo

```python
def SetGroupInfo(group_id: int,
                 group_name: str,
                 flags: int = GROUP_INFO_FLAG_PER_GROUP_ADDRESS_POLICY)
```

Adds or updates a group entry in the controller's GroupDataProvider for this fabric.

**Arguments**:

- `group_id` - The group identifier.
- `group_name` - Human-readable group name.
- `flags` - GroupInfo flags bitmask (kHasAuxiliaryACL=0x01, kMcastAddrPolicy=0x02).
  Defaults to 0x02 (kFlagsDefault).
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.AddGroupEndpoint"></a>

#### AddGroupEndpoint

```python
def AddGroupEndpoint(group_id: int, endpoint_id: int)
```

Associates an endpoint with a group in the controller's GroupDataProvider for this fabric.

**Arguments**:

- `group_id` - The group identifier.
- `endpoint_id` - The endpoint to add to the group.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.SetGroupKey"></a>

#### SetGroupKey

```python
def SetGroupKey(group_id: int, keyset_id: int)
```

Maps a group to a key set in the controller's GroupDataProvider for this fabric.

**Arguments**:

- `group_id` - The group identifier.
- `keyset_id` - The key set identifier to associate with the group.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.RemoveGroupInfo"></a>

#### RemoveGroupInfo

```python
def RemoveGroupInfo(group_id: int)
```

Removes a group entry from the controller's GroupDataProvider for this fabric.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.RemoveKeySet"></a>

#### RemoveKeySet

```python
def RemoveKeySet(keyset_id: int)
```

Removes a KeySet from the controller's GroupDataProvider for this fabric.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.RemoveGroupKeys"></a>

#### RemoveGroupKeys

```python
def RemoveGroupKeys()
```

Removes all GroupKey mappings from the controller's GroupDataProvider for this fabric.

<a id="matter.ChipDeviceCtrl.ChipDeviceControllerBase.CreateManualCode"></a>

#### CreateManualCode

```python
def CreateManualCode(discriminator: int, passcode: int) -> str
```

Creates a standard flow manual code from the given discriminator and passcode.

**Arguments**:

- `discriminator` _int_ - The long discriminator for the DNS-SD advertisement. Valid range: 0-4095.
- `passcode` _int_ - The setup passcode of the device.
  

**Returns**:

- `str` - The decoded string from the buffer.
  

**Raises**:

- `MemoryError` - If the output size is invalid during manual code creation.

<a id="matter.ChipDeviceCtrl.ChipDeviceController"></a>

## ChipDeviceController

```python
class ChipDeviceController(ChipDeviceControllerBase)
```

The ChipDeviceCommissioner binding, named as ChipDeviceController

<a id="matter.ChipDeviceCtrl.ChipDeviceController.Commission"></a>

#### Commission

```python
async def Commission(nodeId: int) -> int
```

Start the auto-commissioning process on a node after establishing a PASE connection.
This function is intended to be used in conjunction with one of the EstablishPASESession
functions. It can be called either before or after the DevicePairingDelegate
receives the OnPairingComplete call. Commissioners that want to perform simple
auto-commissioning should use the supplied "CommissionWithCode" function, which will
establish the PASE connection and commission automatically.

**Arguments**:

- `nodeId` _int_ - The node ID of the device.
  

**Raises**:

  A ChipStackError on failure.
  

**Returns**:

- `int` - Effective Node ID of the device (as defined by the assigned NOC).

<a id="matter.ChipDeviceCtrl.ChipDeviceController.CommissionBleThread"></a>

#### CommissionBleThread

```python
async def CommissionBleThread(discriminator,
                              setupPinCode,
                              nodeId: int,
                              threadOperationalDataset: bytes,
                              isShortDiscriminator: bool = False) -> int
```

Commissions a Thread device over BLE.

**Arguments**:

- `discriminator` _int_ - The long discriminator for the DNS-SD advertisement. Valid range: 0-4095.
- `setupPinCode` _int_ - The setup pin code of the device.
- `nodeId` _int_ - The node ID of the device.
- `threadOperationalDataset` _bytes_ - The Thread operational dataset for commissioning.
- `isShortDiscriminator` _bool_ - Short discriminator.
  

**Returns**:

- `int` - Effective Node ID of the device (as defined by the assigned NOC).

<a id="matter.ChipDeviceCtrl.ChipDeviceController.CommissionNfcThread"></a>

#### CommissionNfcThread

```python
async def CommissionNfcThread(discriminator, setupPinCode, nodeId: int,
                              threadOperationalDataset: bytes) -> int
```

Commissions a Thread device over NFC.

**Arguments**:

- `discriminator` _int_ - The long discriminator for the DNS-SD advertisement. Valid range: 0-4095.
- `setupPinCode` _int_ - The setup pin code of the device.
- `nodeId` _int_ - The node ID of the device.
- `threadOperationalDataset` _bytes_ - The Thread operational dataset for commissioning.
  

**Returns**:

- `int` - Effective Node ID of the device (as defined by the assigned NOC).

<a id="matter.ChipDeviceCtrl.ChipDeviceController.CommissionNfcWiFi"></a>

#### CommissionNfcWiFi

```python
async def CommissionNfcWiFi(discriminator, setupPinCode, nodeId: int,
                            ssid: str, credentials: str) -> int
```

Commissions a Wi-Fi device over NFC.

**Arguments**:

- `discriminator` _int_ - The long discriminator for the DNS-SD advertisement. Valid range: 0-4095.
- `setupPinCode` _int_ - The setup pin code of the device.
- `nodeId` _int_ - The node ID of the device.
- `ssid` _str_ - SSID of the WiFi network.
- `credentials` _str_ - WiFi network password.
  

**Returns**:

- `int` - Effective Node ID of the device (as defined by the assigned NOC).

<a id="matter.ChipDeviceCtrl.ChipDeviceController.CommissionNfcEthernet"></a>

#### CommissionNfcEthernet

```python
async def CommissionNfcEthernet(discriminator, setupPinCode,
                                nodeId: int) -> int
```

Commissions an Ethernet device over NFC.

**Arguments**:

- `discriminator` _int_ - The long discriminator for the DNS-SD advertisement. Valid range: 0-4095.
- `setupPinCode` _int_ - The setup pin code of the device.
- `nodeId` _int_ - The node ID of the device.
  

**Returns**:

- `int` - Effective Node ID of the device (as defined by the assigned NOC).

<a id="matter.ChipDeviceCtrl.ChipDeviceController.CommissionBleWiFi"></a>

#### CommissionBleWiFi

```python
async def CommissionBleWiFi(discriminator,
                            setupPinCode,
                            nodeId: int,
                            ssid: str,
                            credentials: str,
                            isShortDiscriminator: bool = False) -> int
```

Commissions a Wi-Fi device over BLE.

**Arguments**:

- `discriminator` _int_ - The long discriminator for the DNS-SD advertisement. Valid range: 0-4095.
- `setupPinCode` _int_ - The setup pin code of the device.
- `nodeId` _int_ - The node ID of the device.
- `ssid` _str_ - SSID of the WiFi  network.
- `credentials` _str_ - WiFi network password.
- `isShortDiscriminator` _bool_ - Short discriminator.
  

**Returns**:

- `int` - Effective Node ID of the device (as defined by the assigned NOC).

<a id="matter.ChipDeviceCtrl.ChipDeviceController.SetWiFiCredentials"></a>

#### SetWiFiCredentials

```python
def SetWiFiCredentials(ssid: str, credentials: str)
```

Set the Wi-Fi credentials to set during commissioning.

**Arguments**:

- `ssid` _str_ - SSID of the WiFi  network.
- `credentials` _str_ - WiFi network password.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.SetThreadOperationalDataset"></a>

#### SetThreadOperationalDataset

```python
def SetThreadOperationalDataset(threadOperationalDataset)
```

Set the Thread operational dataset to set during commissioning.

**Arguments**:

- `threadOperationalDataset` _bytes_ - The Thread operational dataset for commissioning.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.ResetCommissioningParameters"></a>

#### ResetCommissioningParameters

```python
def ResetCommissioningParameters()
```

Sets the commissioning parameters back to the default values.

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.SetTimeZone"></a>

#### SetTimeZone

```python
def SetTimeZone(offset: int, validAt: int, name: str = "")
```

Set the time zone to set during commissioning. Currently only one time zone entry is supported.

**Arguments**:

- `offset` _int_ - Timezone offset.
- `validAt` _int_ - Timestamp of the timezone.
- `name` _str_ - Name or label of the timezone.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.SetDSTOffset"></a>

#### SetDSTOffset

```python
def SetDSTOffset(offset: int, validStarting: int, validUntil: int)
```

Set the DST offset to set during commissioning. Currently only one DST entry is supported.

**Arguments**:

- `offset` _int_ - Timezone offset.
- `validStarting` _int_ - The start timestamp.
- `validUntil` _int_ - The end timestamp
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.SetTCAcknowledgements"></a>

#### SetTCAcknowledgements

```python
def SetTCAcknowledgements(tcAcceptedVersion: int, tcUserResponse: int)
```

Set the TC acknowledgements to set during commissioning.

**Arguments**:

- `tcAcceptedVersion` _int_ - TC accepted version.
- `tcUserResponse` _int_ - TC user responde.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.SetSkipCommissioningComplete"></a>

#### SetSkipCommissioningComplete

```python
def SetSkipCommissioningComplete(skipCommissioningComplete: bool)
```

Set whether to skip the commissioning complete callback.

**Arguments**:

- `skipCommissioningComplete` _bool_ - The value skip the commissioning complete.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.SetDefaultNTP"></a>

#### SetDefaultNTP

```python
def SetDefaultNTP(defaultNTP: str)
```

Set the DefaultNTP to set during commissioning.

**Arguments**:

- `defaultNTP` _str_ - The default NTP.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.SetTrustedTimeSource"></a>

#### SetTrustedTimeSource

```python
def SetTrustedTimeSource(nodeId: int, endpoint: int)
```

Set the trusted time source nodeId to set during commissioning. This must be a node on the commissioner fabric.

**Arguments**:

- `nodeId` _int_ - The node ID of the device.
- `endpoint` _int_ - endpoint of the device.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.SetCheckMatchingFabric"></a>

#### SetCheckMatchingFabric

```python
def SetCheckMatchingFabric(check: bool)
```

Instructs the auto-commissioner to perform a matching fabric check before commissioning.

**Arguments**:

- `check` _bool_ - Validation fabric before commissioning.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.GenerateICDRegistrationParameters"></a>

#### GenerateICDRegistrationParameters

```python
def GenerateICDRegistrationParameters()
```

Generates ICD registration parameters for this controller.

**Returns**:

- `ICDRegistrationParameters` - An object containing the generated parameters
  including symmetricKey, checkInNodeId, monitoredSubject, stayActiveMs,
  and clientType.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.EnableICDRegistration"></a>

#### EnableICDRegistration

```python
def EnableICDRegistration(parameters: ICDRegistrationParameters)
```

Enables ICD registration for the following commissioning session.

**Arguments**:

- `parameters` - A ICDRegistrationParameters for the parameters used for ICD registration, or None for default arguments.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.DisableICDRegistration"></a>

#### DisableICDRegistration

```python
def DisableICDRegistration()
```

Disables ICD registration.

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.GetFabricCheckResult"></a>

#### GetFabricCheckResult

```python
def GetFabricCheckResult() -> int
```

Returns the fabric check result if SetCheckMatchingFabric was used.

**Returns**:

- `int` - The fabric check result, or `-1` if no check was performed.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.CommissionOnNetwork"></a>

#### CommissionOnNetwork

```python
async def CommissionOnNetwork(
        nodeId: int,
        setupPinCode: int,
        filterType: DiscoveryFilterType = DiscoveryFilterType.NONE,
        filter: typing.Any = None,
        discoveryTimeoutMsec: int = 30000) -> int
```

Does the routine for OnNetworkCommissioning, with a filter for mDNS discovery.
Supported filters are:

DiscoveryFilterType.NONE
DiscoveryFilterType.SHORT_DISCRIMINATOR
DiscoveryFilterType.LONG_DISCRIMINATOR
DiscoveryFilterType.VENDOR_ID
DiscoveryFilterType.DEVICE_TYPE
DiscoveryFilterType.COMMISSIONING_MODE
DiscoveryFilterType.INSTANCE_NAME
DiscoveryFilterType.COMMISSIONER
DiscoveryFilterType.COMPRESSED_FABRIC_ID

The filter can be an integer, a string or None depending on the actual type of selected filter.

**Raises**:

- `ChipStackError` - On failure.
  

**Returns**:

  - Effective Node ID of the device (as defined by the assigned NOC)

<a id="matter.ChipDeviceCtrl.ChipDeviceController.CommissionThreadMeshcop"></a>

#### CommissionThreadMeshcop

```python
async def CommissionThreadMeshcop(nodeId: int, setupPinCode: int,
                                  discriminator: int, borderAgentIPAddr: str,
                                  borderAgentPort: int,
                                  threadOperationalDataset: bytes) -> int
```

Commission with the given node ID from the setupPinCode and discriminator
over Thread MeshCoP transport

**Arguments**:

- `nodeId` _int_ - The node ID of the device.
- `setupPinCode` _int_ - The setup pin code of the device.
- `discriminator` _int_ - The long discriminator for the DNS-SD advertisement. Valid range: 0-4095.
- `borderAgentIPAddr` _str_ - IP address of Border Agent in Thread network
- `borderAgentPort` _int_ - The port of Border Agent in Thread network
- `threadOperationalDataset` _bytes_ - The operational dataset of Thread network

<a id="matter.ChipDeviceCtrl.ChipDeviceController.CommissionViaProxy"></a>

#### CommissionViaProxy

```python
async def CommissionViaProxy(*,
                             proxyNodeId: int,
                             proxySessionId: int,
                             remoteNodeId: int,
                             discriminator: int,
                             setupPinCode: int,
                             proxyEndpoint: int = 1) -> int
```

Commission a device through a Commissioning Proxy.

The proxy CASE session must already exist (proxyNodeId is commissioned
to this controller's fabric) and a ProxyConnectRequest must have been
sent separately to obtain proxySessionId.

WiFi credentials must be set via SetWiFiCredentials() before calling
this method (same pattern as CommissionOnNetwork).

**Arguments**:

- `proxyNodeId` - Node ID of the Commissioning Proxy (DUT).
- `proxySessionId` - SessionId from the ProxyConnectResponse.
- `remoteNodeId` - Node ID to assign to the commissioned ED.
- `discriminator` - Long discriminator of the ED.
- `setupPinCode` - PASE passcode of the ED.
- `proxyEndpoint` - Endpoint on which the CommissioningProxy cluster is hosted (default 1).
  

**Returns**:

  Effective Node ID of the commissioned ED.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.get_rcac"></a>

#### get\_rcac

```python
def get_rcac()
```

Passes captured RCAC data back to Python test modules for validation
- Setting buffer size to max size mentioned in spec:
- Ref: https://github.com/CHIP-Specifications/connectedhomeip-spec/blob/06c4d55962954546ecf093c221fe1dab57645028/policies/matter_certificate_policy.adoc#615-key-sizes

**Returns**:

- `bytes` - A bytes sentence representing the RCAC, or None if no data.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.CommissionWithCode"></a>

#### CommissionWithCode

```python
async def CommissionWithCode(
        setupPayload: str,
        nodeId: int,
        discoveryType: DiscoveryType = DiscoveryType.DISCOVERY_ALL) -> int
```

Commission with the given node ID from the setupPayload.
setupPayload may be a QR or manual code.

**Arguments**:

- `setupPayload` _str_ - The setup payload (QR or manual code).
- `nodeId` _int_ - The node ID of the device.
- `discoveryType` _DiscoveryType.DISCOVERY_ALL_ - The discovery type to use.
  

**Raises**:

- `ChipStackError` - On failure.
  

**Returns**:

- `int` - Effective Node ID of the device (as defined by the assigned NOC)

<a id="matter.ChipDeviceCtrl.ChipDeviceController.NOCChainCallback"></a>

#### NOCChainCallback

```python
def NOCChainCallback(nocChain)
```

Callback function for handling the NOC chain result.

**Arguments**:

- `nocChain` _nocChain_ - The object NOC chain data received.
  

**Returns**:

  None

<a id="matter.ChipDeviceCtrl.ChipDeviceController.IssueNOCChain"></a>

#### IssueNOCChain

```python
async def IssueNOCChain(
        csr: Clusters.OperationalCredentials.Commands.CSRResponse,
        nodeId: int)
```

Issue an NOC chain using the associated OperationalCredentialsDelegate.
The NOC chain will be provided in TLV cert format.

**Arguments**:

- `crs` _cluster_ - Certificate Signing Request response
- `nodeId` _int_ - The node ID of the device.
  

**Returns**:

- `asyncio.Future` - A future object that is the result of the NOC Chain operation.

<a id="matter.ChipDeviceCtrl.ChipDeviceController.SetDACRevocationSetPath"></a>

#### SetDACRevocationSetPath

```python
def SetDACRevocationSetPath(dacRevocationSetPath: str | None)
```

Set the path to the device attestation revocation set JSON file.

**Arguments**:

- `dacRevocationSetPath` _Optional[str]_ - Path to the JSON file containing the device attestation revocation set.
  

**Raises**:

- `ChipStackError` - On failure.

<a id="matter.ChipDeviceCtrl.BareChipDeviceController"></a>

## BareChipDeviceController

```python
class BareChipDeviceController(ChipDeviceControllerBase)
```

A bare device controller without AutoCommissioner support.

<a id="matter.ChipDeviceCtrl.BareChipDeviceController.__init__"></a>

#### \_\_init\_\_

```python
def __init__(operationalKey: p256keypair.P256Keypair,
             noc: bytes,
             icac: bytes | None,
             rcac: bytes,
             ipk: bytes | None,
             adminVendorId: int,
             name: str | None = None)
```

Creates a controller without AutoCommissioner.

The allocated controller uses the noc, icac, rcac and ipk instead of the default,
random generated certificates / keys. Which is suitable for creating a controller
for manually signing certificates for testing.

**Arguments**:

- `operationalKey` - A P256Keypair object for the operational key of the controller.
- `noc` _bytes_ - The NOC for the controller, in bytes.
- `icac` _Optional[bytes]_ - The optional ICAC for the controller.
- `rcac` _bytes_ - The RCAC for the controller.
- `ipk` _Optional[bytes]_ - The optional IPK for the controller, when None is provided, the defaultIpk will be used.
- `adminVendorId` _int_ - The adminVendorId of the controller.
- `name` _str_ - The name of the controller, for debugging use only.
  

**Raises**:

- `ChipStackError` - On failure

