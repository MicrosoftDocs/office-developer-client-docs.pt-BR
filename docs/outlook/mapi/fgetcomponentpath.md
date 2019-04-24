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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3456d81935a0a94bc2158eefd321da968dda9983
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335207"
---
# <a name="fgetcomponentpath"></a><span data-ttu-id="7f448-103">FGetComponentPath</span><span class="sxs-lookup"><span data-stu-id="7f448-103">FGetComponentPath</span></span>

  
  
<span data-ttu-id="7f448-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f448-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f448-105">Retorna o caminho para o Mapi32. dll privado.</span><span class="sxs-lookup"><span data-stu-id="7f448-105">Returns the path to the private Mapi32.dll.</span></span>
  
```cpp
BOOL FGetComponentPath(
  LPCSTR szComponent,
  LPSTR szQualifier,
  LPSTR szDllPath,
  DWORD cchBufferSize,
  BOOL fInstall
);
```

## <a name="parameters"></a><span data-ttu-id="7f448-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f448-106">Parameters</span></span>

 <span data-ttu-id="7f448-107">_szComponent_</span><span class="sxs-lookup"><span data-stu-id="7f448-107">_szComponent_</span></span>
  
> <span data-ttu-id="7f448-108">no A chave do registro MSIComponentID descrita nas [configurações de stub Mapi32. dll](https://msdn.microsoft.com/library/dd162409.aspx).</span><span class="sxs-lookup"><span data-stu-id="7f448-108">[in] The MSIComponentID reg key described in [Mapi32.dll Stub Registry Settings](https://msdn.microsoft.com/library/dd162409.aspx).</span></span>
    
 <span data-ttu-id="7f448-109">_szQualifier_</span><span class="sxs-lookup"><span data-stu-id="7f448-109">_szQualifier_</span></span>
  
> <span data-ttu-id="7f448-110">no A subchave MSIApplicationLCID ou MSIOfficeLCID descrita em [escolher uma versão específica de MAPI a ser carregada](how-to-choose-a-specific-version-of-mapi-to-load.md).</span><span class="sxs-lookup"><span data-stu-id="7f448-110">[in] The MSIApplicationLCID or MSIOfficeLCID subkey described in [Choose a Specific Version of MAPI to Load](how-to-choose-a-specific-version-of-mapi-to-load.md).</span></span> <span data-ttu-id="7f448-111">Os chamadores podem passar **NULL** se não houver nenhum qualificador.</span><span class="sxs-lookup"><span data-stu-id="7f448-111">Callers can pass **null** if there is no qualifier.</span></span> 
    
 <span data-ttu-id="7f448-112">_szDllPath_</span><span class="sxs-lookup"><span data-stu-id="7f448-112">_szDllPath_</span></span>
  
> <span data-ttu-id="7f448-113">no O caminho para o Mapi32. dll privado, que tem a funcionalidade MAPI total (as mesmas exportações que o Mapi32. dll).</span><span class="sxs-lookup"><span data-stu-id="7f448-113">[in] The path to the private Mapi32.dll, which has full MAPI functionality (the same exports as the Mapi32.dll).</span></span>
    
 <span data-ttu-id="7f448-114">_cchBufferSize_</span><span class="sxs-lookup"><span data-stu-id="7f448-114">_cchBufferSize_</span></span>
  
> <span data-ttu-id="7f448-115">no O tamanho de _szDllPath_, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="7f448-115">[in] The size of  _szDllPath_, in characters.</span></span>
    
 <span data-ttu-id="7f448-116">_fInstall_</span><span class="sxs-lookup"><span data-stu-id="7f448-116">_fInstall_</span></span>
  
> <span data-ttu-id="7f448-117">no Informa ao MAPI para instalar o componente Mapi32. dll privado se ele estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="7f448-117">[in] Tells MAPI to install the private Mapi32.dll component if it is absent.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7f448-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7f448-118">Return value</span></span>

 <span data-ttu-id="7f448-119">**verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="7f448-119">**true**</span></span>
  
> <span data-ttu-id="7f448-120">O caminho foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="7f448-120">The path was found.</span></span>
    
 <span data-ttu-id="7f448-121">**false**</span><span class="sxs-lookup"><span data-stu-id="7f448-121">**false**</span></span>
  
> <span data-ttu-id="7f448-122">O caminho não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="7f448-122">The path was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f448-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f448-123">Remarks</span></span>

<span data-ttu-id="7f448-124">Use a função **FGetComponentPath** quando precisar obter o caminho para o Mapi32. dll privado.</span><span class="sxs-lookup"><span data-stu-id="7f448-124">Use the **FGetComponentPath** function when you need to get the path to the private Mapi32.dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f448-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f448-125">See also</span></span>



[<span data-ttu-id="7f448-126">Escolher uma versão específica de MAPI para carregar</span><span class="sxs-lookup"><span data-stu-id="7f448-126">Choose a Specific Version of MAPI to Load</span></span>](how-to-choose-a-specific-version-of-mapi-to-load.md)


[<span data-ttu-id="7f448-127">Configurações do registro stub Mapi32. dll</span><span class="sxs-lookup"><span data-stu-id="7f448-127">Mapi32.dll Stub Registry Settings</span></span>](https://msdn.microsoft.com/library/dd162409.aspx)

