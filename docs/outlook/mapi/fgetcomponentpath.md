---
title: FGetComponentPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FGetComponentPath
api_type:
- COM
ms.assetid: 2a303458-3283-409a-bc3b-b891f3fcfc22
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e4bce7f122522532023d18b43fe4bfdeda84af9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766537"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="bd1b9-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="bd1b9-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="bd1b9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd1b9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd1b9-105">Retorna o caminho para o Mapi32 privada.</span><span class="sxs-lookup"><span data-stu-id="bd1b9-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="bd1b9-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="bd1b9-106">Parameters</span></span>

 <span data-ttu-id="bd1b9-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="bd1b9-107">_szComponent_</span></span>
  
> <span data-ttu-id="bd1b9-108">[in] A chave do registro MSIComponentID descrito nas [Configurações de registro de Stub Mapi32](http://msdn.microsoft.com/pt-br/library/dd162409.aspx).</span><span class="sxs-lookup"><span data-stu-id="bd1b9-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](http://msdn.microsoft.com/pt-br/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="bd1b9-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="bd1b9-109">_szQualifier_</span></span>
  
> <span data-ttu-id="bd1b9-110">[in] A subchave MSIApplicationLCID ou MSIOfficeLCID descrita na [Escolha de uma versão específica de MAPI a carga](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="bd1b9-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="bd1b9-111">Os chamadores podem passar **null** se não houver nenhum qualificador.</span><span class="sxs-lookup"><span data-stu-id="bd1b9-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="bd1b9-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="bd1b9-112">_szDllPath_</span></span>
  
> <span data-ttu-id="bd1b9-113">[in] O caminho para o Mapi32 privada, que tem a funcionalidade total do MAPI (as exportações mesmas como o Mapi32).</span><span class="sxs-lookup"><span data-stu-id="bd1b9-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="bd1b9-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="bd1b9-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="bd1b9-115">[in] O tamanho da _szDllPath_, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="bd1b9-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="bd1b9-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="bd1b9-116">_fInstall_</span></span>
  
> <span data-ttu-id="bd1b9-117">[in] Informa MAPI para instalar o componente de Mapi32 privado se ele está ausente.</span><span class="sxs-lookup"><span data-stu-id="bd1b9-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bd1b9-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bd1b9-118">Return value</span></span>

 <span data-ttu-id="bd1b9-119">**True**</span><span class="sxs-lookup"><span data-stu-id="bd1b9-119">**true**</span></span>
  
> <span data-ttu-id="bd1b9-120">O caminho foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="bd1b9-120">The path was found.</span></span>
    
 <span data-ttu-id="bd1b9-121">**False**</span><span class="sxs-lookup"><span data-stu-id="bd1b9-121">**false**</span></span>
  
> <span data-ttu-id="bd1b9-122">O caminho não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="bd1b9-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd1b9-123">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="bd1b9-123">Remarks</span></span>

<span data-ttu-id="bd1b9-124">Use a função de **FGetComponentPath** quando precisar fazer o caminho para o Mapi32 privada.</span><span class="sxs-lookup"><span data-stu-id="bd1b9-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bd1b9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd1b9-125">See also</span></span>



[<span data-ttu-id="bd1b9-126">Escolher uma versão específica de MAPI para carga</span><span class="sxs-lookup"><span data-stu-id="bd1b9-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="bd1b9-127">Configurações de registro de Stub Mapi32</span><span class="sxs-lookup"><span data-stu-id="bd1b9-127">Mapi32.dll Stub Registry Settings</span></span>](http://msdn.microsoft.com/pt-br/library/dd162409.aspx)

