---
title: IPSTOVERRIDEREQRegisterTrustedPSTOverrideHandler
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ.RegisterTrustedPSTOverrideHandler
api_type:
- COM
ms.assetid: 4a73c77c-7e32-4302-bffe-a1ea13574731
description: 'Modificado em: 24 de fevereiro de 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393870"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="dab24-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="dab24-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="dab24-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dab24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dab24-105">Inicia o procedimento desbloqueando um arquivo de pastas particulares (. pst).</span><span class="sxs-lookup"><span data-stu-id="dab24-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="dab24-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dab24-106">Parameters</span></span>

 <span data-ttu-id="dab24-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="dab24-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="dab24-108">[in] Um ponteiro para o caminho de uma biblioteca de vínculo dinâmico (DLL) de terceiros.</span><span class="sxs-lookup"><span data-stu-id="dab24-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="dab24-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="dab24-109">_pvClientData_</span></span>
  
> <span data-ttu-id="dab24-110">[in] Um ponteiro para dados de cliente, que serão passados pelo provedor de PST para chamadas subsequentes à função de HrTrustedPSTOverrideHandlerCallback da DLL.</span><span class="sxs-lookup"><span data-stu-id="dab24-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="dab24-111">Esses dados do cliente podem ser usados pela DLL para auxiliar verificando se o PST deve ser desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="dab24-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dab24-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dab24-112">Return value</span></span>

<span data-ttu-id="dab24-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="dab24-113">S_OK</span></span>
  
> <span data-ttu-id="dab24-114">A chamada de função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="dab24-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dab24-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="dab24-115">Remarks</span></span>

<span data-ttu-id="dab24-116">A DLL especificada pelo parâmetro wzDllPath deve estar conectada usando um certificado digital.</span><span class="sxs-lookup"><span data-stu-id="dab24-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="dab24-117">A DLL também deve exportar uma função com a seguinte assinatura.</span><span class="sxs-lookup"><span data-stu-id="dab24-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="dab24-118">Essa função será chamada com um ponteiro para o objeto IMsgStore para o PST, um ponteiro para um objeto IUnknown que implementa a interface IPSTOVERRIDE1 e um ponteiro para os dados originalmente fornecidos pelo pvClientData.</span><span class="sxs-lookup"><span data-stu-id="dab24-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="dab24-119">Para obter mais informações, consulte [como implementar um manipulador de substituição de PST para ignorar a política PSTDisableGrow no Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="dab24-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dab24-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="dab24-120">See also</span></span>



[<span data-ttu-id="dab24-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dab24-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="dab24-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dab24-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

