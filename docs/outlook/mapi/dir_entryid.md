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
ms.openlocfilehash: e7abcb2c86ff5cabe0b8f5664ec316244617ac09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421232"
---
# <a name="dir_entryid"></a><span data-ttu-id="c06b8-103">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c06b8-103">DIR_ENTRYID</span></span>

  
  
<span data-ttu-id="c06b8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c06b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c06b8-105">Descreve as propriedades de uma ID de entrada de diretório.</span><span class="sxs-lookup"><span data-stu-id="c06b8-105">Describes the properties of a directory entry id.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c06b8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c06b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="c06b8-107">entryid.h</span><span class="sxs-lookup"><span data-stu-id="c06b8-107">entryid.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="c06b8-108">Members</span><span class="sxs-lookup"><span data-stu-id="c06b8-108">Members</span></span>

 <span data-ttu-id="c06b8-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="c06b8-109">**abFlags**</span></span>
  
> <span data-ttu-id="c06b8-110">Uma bitmask de sinalizadores que fornece informações que descrevem o objeto.</span><span class="sxs-lookup"><span data-stu-id="c06b8-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="c06b8-111">Para obter mais informações, consulte a descrição do **campo abFlags** de uma [estrutura ENTRYID.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="c06b8-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="c06b8-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="c06b8-112">**muid**</span></span>
  
> <span data-ttu-id="c06b8-113">GUID que identifica o provedor do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c06b8-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="c06b8-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="c06b8-114">**ulVersion**</span></span>
  
> <span data-ttu-id="c06b8-115">O número da versão da **DIR_ENTRYID** estrutura.</span><span class="sxs-lookup"><span data-stu-id="c06b8-115">The version number of the **DIR_ENTRYID** structure.</span></span> <span data-ttu-id="c06b8-116">Deve ser definido como CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="c06b8-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="c06b8-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="c06b8-117">**ulType**</span></span>
  
> <span data-ttu-id="c06b8-118">Um inteiro que representa o tipo de ID de entrada de diretório.</span><span class="sxs-lookup"><span data-stu-id="c06b8-118">An integer representing the directory entry ID type.</span></span> <span data-ttu-id="c06b8-119">Deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c06b8-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="c06b8-120">**Nome**</span><span class="sxs-lookup"><span data-stu-id="c06b8-120">**Name**</span></span>|<span data-ttu-id="c06b8-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c06b8-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c06b8-122">CONTAB_ROOT</span><span class="sxs-lookup"><span data-stu-id="c06b8-122">CONTAB_ROOT</span></span>  <br/> |<span data-ttu-id="c06b8-123">A pasta raiz de um livro de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="c06b8-123">The root folder for a MAPI address book.</span></span>  <br/> |
|<span data-ttu-id="c06b8-124">CONTAB_SUBROOT</span><span class="sxs-lookup"><span data-stu-id="c06b8-124">CONTAB_SUBROOT</span></span>  <br/> |<span data-ttu-id="c06b8-125">Uma subpasta contida na pasta raiz do objeto de catálogos de endereços MAPI.</span><span class="sxs-lookup"><span data-stu-id="c06b8-125">A subfolder contained within the root folder of the MAPI address book object.</span></span>  <br/> |
|<span data-ttu-id="c06b8-126">CONTAB_CONTAINER</span><span class="sxs-lookup"><span data-stu-id="c06b8-126">CONTAB_CONTAINER</span></span>  <br/> |<span data-ttu-id="c06b8-127">Abrir o contêiner de um objeto do catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="c06b8-127">An address book container object.</span></span>  <br/> |
   
 <span data-ttu-id="c06b8-128">**muidID**</span><span class="sxs-lookup"><span data-stu-id="c06b8-128">**muidID**</span></span>
  
> <span data-ttu-id="c06b8-129">Um GUID que identifica o objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="c06b8-129">A GUID that identifies the logon object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c06b8-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="c06b8-130">Remarks</span></span>

<span data-ttu-id="c06b8-131">As **estruturas DIR_ENTRYID** [e CONTAB_ENTRYID](contab_entryid.md) são idênticas, exceto para o **membro ulType.**</span><span class="sxs-lookup"><span data-stu-id="c06b8-131">The structures **DIR_ENTRYID** and [CONTAB_ENTRYID](contab_entryid.md) are identical, except for the **ulType** member.</span></span> <span data-ttu-id="c06b8-132">O conteúdo do membro **ulType** determina qual estrutura é apropriada para os campos restantes.</span><span class="sxs-lookup"><span data-stu-id="c06b8-132">The contents of the **ulType** member determine which structure is appropriate for the remaining fields.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c06b8-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c06b8-133">See also</span></span>



[<span data-ttu-id="c06b8-134">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="c06b8-134">CONTAB_ENTRYID</span></span>](contab_entryid.md)


[<span data-ttu-id="c06b8-135">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c06b8-135">MAPI Structures</span></span>](mapi-structures.md)

