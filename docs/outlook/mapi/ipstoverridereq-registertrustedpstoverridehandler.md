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
ms.openlocfilehash: 4fc3b7427fc13a024aab38c7b7df1d940a4730ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767678"
---
# <a name="ipstoverridereqregistertrustedpstoverridehandler"></a><span data-ttu-id="656ac-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span><span class="sxs-lookup"><span data-stu-id="656ac-103">IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler</span></span>

 
  
<span data-ttu-id="656ac-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="656ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="656ac-105">Inicia o procedimento desbloqueando um arquivo de pastas particulares (. pst).</span><span class="sxs-lookup"><span data-stu-id="656ac-105">Initiates the unlocking procedure for a Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT RegisterTrustedPSTOverrideHandler (
  LPCWSTR pwzDllPath, 
  LPVOID pvClientData
); 

```

## <a name="parameters"></a><span data-ttu-id="656ac-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="656ac-106">Parameters</span></span>

 <span data-ttu-id="656ac-107">_pwzDllPath_</span><span class="sxs-lookup"><span data-stu-id="656ac-107">_pwzDllPath_</span></span>
  
> <span data-ttu-id="656ac-108">[in] Um ponteiro para o caminho de uma biblioteca de vínculo dinâmico (DLL) de terceiros.</span><span class="sxs-lookup"><span data-stu-id="656ac-108">[in] A pointer to the path of a third-party dynamic-link library (DLL).</span></span>
    
 <span data-ttu-id="656ac-109">_pvClientData_</span><span class="sxs-lookup"><span data-stu-id="656ac-109">_pvClientData_</span></span>
  
> <span data-ttu-id="656ac-110">[in] Um ponteiro para dados de cliente, que serão passados pelo provedor de PST para chamadas subsequentes à função de HrTrustedPSTOverrideHandlerCallback da DLL.</span><span class="sxs-lookup"><span data-stu-id="656ac-110">[in] A pointer to client data, which will be passed by the PST provider into subsequent calls to the DLL's HrTrustedPSTOverrideHandlerCallback function.</span></span> <span data-ttu-id="656ac-111">Esses dados do cliente podem ser usados pela DLL para auxiliar verificando se o PST deve ser desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="656ac-111">This client data may be used by the DLL to assist in verifying whether the PST should be unlocked.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="656ac-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="656ac-112">Return value</span></span>

<span data-ttu-id="656ac-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="656ac-113">S_OK</span></span>
  
> <span data-ttu-id="656ac-114">A chamada de função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="656ac-114">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="656ac-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="656ac-115">Remarks</span></span>

<span data-ttu-id="656ac-116">A DLL especificada pelo parâmetro wzDllPath deve estar conectada usando um certificado digital.</span><span class="sxs-lookup"><span data-stu-id="656ac-116">The DLL specified by the wzDllPath parameter must be signed using a digital certificate.</span></span> <span data-ttu-id="656ac-117">A DLL também deve exportar uma função com a seguinte assinatura.</span><span class="sxs-lookup"><span data-stu-id="656ac-117">The DLL must also export a function with the following signature.</span></span>
  
```
extern "C" HRESULT __cdecl HrTrustedPSTOverrideHandlerCallback(IMsgStore *pmstore, IUnknown *pOverride, LPVOID pvClientData)
```

<span data-ttu-id="656ac-118">Essa função será chamada com um ponteiro para o objeto IMsgStore para o PST, um ponteiro para um objeto IUnknown que implementa a interface IPSTOVERRIDE1 e um ponteiro para os dados originalmente fornecidos pelo pvClientData.</span><span class="sxs-lookup"><span data-stu-id="656ac-118">This function will be called with a pointer to the IMsgStore object for the PST, a pointer to an IUnknown object that implements the IPSTOVERRIDE1 interface, and a pointer to the data originally supplied through pvClientData.</span></span>
  
<span data-ttu-id="656ac-119">Para obter mais informações, consulte [como implementar um manipulador de substituição de PST para ignorar a política PSTDisableGrow no Outlook 2007](http://support.microsoft.com/kb/956070).</span><span class="sxs-lookup"><span data-stu-id="656ac-119">For more information see [How to implement a PST override handler to bypass the PSTDisableGrow policy in Outlook 2007](http://support.microsoft.com/kb/956070).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="656ac-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="656ac-120">See also</span></span>



[<span data-ttu-id="656ac-121">IPSTOVERRIDE1: IUnknown</span><span class="sxs-lookup"><span data-stu-id="656ac-121">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="656ac-122">IPSTOVERRIDEREQ: IUnknown</span><span class="sxs-lookup"><span data-stu-id="656ac-122">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

