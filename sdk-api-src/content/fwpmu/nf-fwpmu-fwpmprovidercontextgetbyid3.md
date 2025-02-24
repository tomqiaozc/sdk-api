---
UID: NF:fwpmu.FwpmProviderContextGetById3
title: FwpmProviderContextGetById3
description: Retrieves a provider context.
tech.root: fwp
ms.date: 05/02/2024
targetos: Windows
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Fwpuclnt.dll
req.header: fwpmu.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Fwpuclnt.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmProviderContextGetById3
f1_keywords:
 - FwpmProviderContextGetById3
 - fwpmu/FwpmProviderContextGetById3
dev_langs:
 - c++
helpviewer_keywords:
 - FwpmProviderContextGetById3
---

## -description

Retrieves a provider context.

## -parameters

### -param engineHandle

Type: \_In\_ **[HANDLE](/windows/win32/winprog/windows-data-types)**

A handle to an open session with the filter engine. To open a session with the filter engine, call [FwpmEngineOpen0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmengineopen0).

### -param id

Type: \_In\_ **[UINT64](/windows/win32/winprog/windows-data-types)**

### -param providerContext

Type: \_Outptr\_ **[FWPM_PROVIDER_CONTEXT3](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context3)\*\***

The provider context object to be added.

## -returns

Type: **[DWORD](/windows/win32/winprog/windows-data-types)\***

|Return code/value|Description|
|-|-|
|ERROR_SUCCESS<br/>0|The provider context was retrieved successfully.|
|FWP_E_* error code<br/>0x80320001—0x80320039|A Windows Filtering Platform (WFP)-specific error. For details, see [WFP error codes](/windows/win32/fwp/wfp-error-codes).|
|RPC_* error code<br/>0x80010001—0x80010122|Failure to communicate with the remote or local firewall engine.|

## -remarks

You must free the returned object by calling [FwpmFreeMemory0](/windows/win32/api/fwpmu/nf-fwpmu-fwpmfreememory0).

To call this function, you need [FWPM_ACTRL_READ](/windows/win32/fwp/access-right-identifiers) access to the provider context. For more info, see [Access control](/windows/win32/fwp/access-control).

## -see-also
