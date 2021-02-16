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
description: 'Última modificação: 24 de fevereiro de 2013'
ms.openlocfilehash: acc0986dd80b549b0cb2b941a6937d47a4a959fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279532"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="2d94d-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="2d94d-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="2d94d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d94d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d94d-105">Inicia o procedimento de desbloqueio para um arquivo de Pastas Particulares (.pst).</span><span class="sxs-lookup"><span data-stu-id="2d94d-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="2d94d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d94d-106">Parameters</span></span>

 <span data-ttu-id="2d94d-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="2d94d-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="2d94d-108">[in] Um ponteiro para o caminho de uma biblioteca de vínculo dinâmico (DLL) de terceiros.</span><span class="sxs-lookup"><span data-stu-id="2d94d-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="2d94d-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="2d94d-109">_pvClientData_</span></span>
  
> <span data-ttu-id="2d94d-110">[in] Um ponteiro para os dados do cliente, que será passado pelo provedor PST para chamadas subsequentes para a função HrTrustedPSTOverrideHandlerCallback da DLL.</span><span class="sxs-lookup"><span data-stu-id="2d94d-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="2d94d-111">Esses dados de cliente podem ser usados pela DLL para ajudar a verificar se o PST deve ser desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="2d94d-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2d94d-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2d94d-112">Return value</span></span>

<span data-ttu-id="2d94d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d94d-113">S_OK</span></span>
  
> <span data-ttu-id="2d94d-114">A chamada de função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2d94d-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2d94d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d94d-115">Remarks</span></span>

<span data-ttu-id="2d94d-116">A DLL especificada pelo parâmetro wzDllPath deve ser assinada usando um certificado digital.</span><span class="sxs-lookup"><span data-stu-id="2d94d-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="2d94d-117">A DLL também deve exportar uma função com a assinatura a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d94d-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="2d94d-118">Essa função será chamada com um ponteiro para o objeto IMsgStore para o PST, um ponteiro para um objeto IUnknown que implementa a interface IPSTOVERRIDE1 e um ponteiro para os dados originalmente fornecidos por meio de pvClientData.</span><span class="sxs-lookup"><span data-stu-id="2d94d-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="2d94d-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="2d94d-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](https://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d94d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d94d-120">See also</span></span>



[<span data-ttu-id="2d94d-121">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d94d-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="2d94d-122">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d94d-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

