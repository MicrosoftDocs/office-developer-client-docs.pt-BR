---
title: DIR_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9e055269-f3bf-4b64-8384-3cbc372c0b34
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9ef3f37ab266469e83434d5d9bd0bc7e2ef897fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583341"
---
# <a name="direntryid"></a><span data-ttu-id="e2e05-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e2e05-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="e2e05-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2e05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2e05-105">Descreve as propriedades de uma identificação de entrada de diretório.</span><span class="sxs-lookup"><span data-stu-id="e2e05-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2e05-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e2e05-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2e05-107">EntryID.h</span><span class="sxs-lookup"><span data-stu-id="e2e05-107">entryid.h</span></span>  <br/> |
   
```cpp
#pragma pack(4)
typedef struct _dir_entryid
{
    BYTE abFlags[4]; 
    MAPIUID muid; 
    ULONG ulVersion; 
    ULONG ulType; 
    MAPIUID muidID; 
}   DIR_ENTRYID, *LPDIR_ENTRYID; 
#pragma pack()
```

## <a name="members"></a><span data-ttu-id="e2e05-108">Members</span><span class="sxs-lookup"><span data-stu-id="e2e05-108">Members</span></span>

 <span data-ttu-id="e2e05-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="e2e05-109">**abFlags**</span></span>
  
> <span data-ttu-id="e2e05-110">Uma bitmask dos sinalizadores que fornece informações que descrevem o objeto.</span><span class="sxs-lookup"><span data-stu-id="e2e05-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="e2e05-111">Para obter mais informações, consulte a descrição do campo **abFlags** de uma estrutura de [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="e2e05-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="e2e05-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="e2e05-112">**muid**</span></span>
  
> <span data-ttu-id="e2e05-113">GUID que identifica o provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e2e05-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="e2e05-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="e2e05-114">**ulVersion**</span></span>
  
> <span data-ttu-id="e2e05-115">O número de versão da estrutura **DIR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="e2e05-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="e2e05-116">Deve ser definida como CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="e2e05-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="e2e05-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="e2e05-117">**ulType**</span></span>
  
> <span data-ttu-id="e2e05-118">Um inteiro que representa o tipo de ID de entrada de diretório.</span><span class="sxs-lookup"><span data-stu-id="e2e05-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="e2e05-119">Ele deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="e2e05-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="e2e05-120">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e2e05-120">**Name**</span></span>|<span data-ttu-id="e2e05-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e2e05-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2e05-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="e2e05-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="e2e05-123">A pasta raiz de um catálogo de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="e2e05-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="e2e05-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="e2e05-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="e2e05-125">Uma subpasta contida na pasta raiz do objeto de catálogo de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="e2e05-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="e2e05-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="e2e05-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="e2e05-127">Um objeto de contêiner de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="e2e05-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="e2e05-128">**muidID**</span><span class="sxs-lookup"><span data-stu-id="e2e05-128">**muidID**</span></span>
  
> <span data-ttu-id="e2e05-129">Um GUID que identifica o objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="e2e05-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2e05-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2e05-130">Remarks</span></span>

<span data-ttu-id="e2e05-131">As estruturas **DIR_ENTRYID** e [CONTAB_ENTRYID](contab_entryid.md) são idênticas, exceto para o membro **ulType** .</span><span class="sxs-lookup"><span data-stu-id="e2e05-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="e2e05-132">O conteúdo do membro **ulType** determinar qual estrutura é apropriada para os campos restantes.</span><span class="sxs-lookup"><span data-stu-id="e2e05-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2e05-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2e05-133">See also</span></span>



[<span data-ttu-id="e2e05-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="e2e05-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="e2e05-135">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="e2e05-135">MAPI Structures</span></span>](mapi-structures.md)

