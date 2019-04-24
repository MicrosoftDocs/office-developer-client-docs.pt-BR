---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a2a204f76b62c8c6bc6d8a4e793c936a0184dc65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335074"
---
# <a name="contabentryid"></a><span data-ttu-id="ec70f-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ec70f-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="ec70f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec70f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec70f-105">Contém a identificação de entrada da pasta contatos.</span><span class="sxs-lookup"><span data-stu-id="ec70f-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ec70f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ec70f-106">Header file:</span></span>  <br/> |<span data-ttu-id="ec70f-107">msomapiutil. h</span><span class="sxs-lookup"><span data-stu-id="ec70f-107">msomapiutil.h</span></span>  <br/> |
   
```cpp
#pragma pack(4) 
typedef struct _contab_entryid
{
    BYTE abFlags[4];
    MAPIUID muid;
    ULONG ulVersion;
    ULONG ulType;
    ULONG ulIndex;
    ULONG cbeid;
    BYTE abeid[1];
}   CONTAB_ENTRYID, *LPCONTAB_ENTRYID;
#pragma pack() 
```

## <a name="members"></a><span data-ttu-id="ec70f-108">Members</span><span class="sxs-lookup"><span data-stu-id="ec70f-108">Members</span></span>

 <span data-ttu-id="ec70f-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="ec70f-109">**abFlags**</span></span>
  
> <span data-ttu-id="ec70f-110">Uma bitmask de sinalizadores que fornece informações que descrevem o objeto.</span><span class="sxs-lookup"><span data-stu-id="ec70f-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="ec70f-111">Para obter mais informações, consulte a descrição do campo **abFlags** de uma estrutura [EntryID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="ec70f-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="ec70f-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="ec70f-112">**muid**</span></span>
  
> <span data-ttu-id="ec70f-113">GUID que identifica o provedor de repositório.</span><span class="sxs-lookup"><span data-stu-id="ec70f-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="ec70f-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="ec70f-114">**ulVersion**</span></span>
  
> <span data-ttu-id="ec70f-115">O número da versão da estrutura **CONTAB_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="ec70f-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="ec70f-116">Deve ser definido como CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="ec70f-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="ec70f-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="ec70f-117">**ulType**</span></span>
  
> <span data-ttu-id="ec70f-118">Um inteiro que representa o tipo de ID de entrada de contato.</span><span class="sxs-lookup"><span data-stu-id="ec70f-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="ec70f-119">Deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ec70f-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="ec70f-120">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ec70f-120">**Name**</span></span>|<span data-ttu-id="ec70f-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ec70f-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ec70f-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="ec70f-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="ec70f-123">Um objeto de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="ec70f-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="ec70f-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="ec70f-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="ec70f-125">0" não é um objeto de lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="ec70f-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="ec70f-126">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="ec70f-126">**ulIndex**</span></span>
  
> <span data-ttu-id="ec70f-127">O índice do subconjunto de propriedades de email.</span><span class="sxs-lookup"><span data-stu-id="ec70f-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="ec70f-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="ec70f-128">**cbeid**</span></span>
  
> <span data-ttu-id="ec70f-129">O tamanho do identificador de entrada da mensagem de contato associada a essa entrada no catálogo de endereços de contatos.</span><span class="sxs-lookup"><span data-stu-id="ec70f-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="ec70f-130">**Abeid**</span><span class="sxs-lookup"><span data-stu-id="ec70f-130">**abeid**</span></span>
  
> <span data-ttu-id="ec70f-131">O identificador de entrada da mensagem de contato associada a essa entrada no catálogo de endereços de contatos.</span><span class="sxs-lookup"><span data-stu-id="ec70f-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec70f-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec70f-132">Remarks</span></span>

<span data-ttu-id="ec70f-133">Um catálogo de endereços de contatos é um catálogo de endereços que contém todos os itens de contato em uma pasta de contatos que tem um endereço de email ou um número de fax.</span><span class="sxs-lookup"><span data-stu-id="ec70f-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="ec70f-134">Cada entrada em um catálogo de endereços de contatos é associada a um endereço de email ou a um número de fax.</span><span class="sxs-lookup"><span data-stu-id="ec70f-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="ec70f-135">Como um item de contato pode ter até três endereços de email e três números de fax, um item de contato pode ser representado por até seis entradas no catálogo de endereços de contatos correspondente.</span><span class="sxs-lookup"><span data-stu-id="ec70f-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="ec70f-136">O objetivo de um catálogo de endereços de contatos é oferecer suporte aos usuários que endereçam mensagens de email para contatos em uma pasta de contatos.</span><span class="sxs-lookup"><span data-stu-id="ec70f-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="ec70f-137">O provedor de catálogo de endereços de contatos que o Microsoft Outlook 2010 e o Microsoft Outlook 2013 oferecem suporte é contab32. dll.</span><span class="sxs-lookup"><span data-stu-id="ec70f-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="ec70f-138">A estrutura **CONTAB_ENTRYID** oferece suporte a um subconjunto das informações presentes na mensagem de contato MAPI subjacente.</span><span class="sxs-lookup"><span data-stu-id="ec70f-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="ec70f-139">Ele identifica a mensagem de contato à qual uma entrada de catálogo de endereços de contatos específica está associada.</span><span class="sxs-lookup"><span data-stu-id="ec70f-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="ec70f-140">Os campos **cbeid** e **Abeid** são válidos somente quando o valor do campo **ulType** é definido como CONTAB_DISTLIST ou CONTAB_USER.</span><span class="sxs-lookup"><span data-stu-id="ec70f-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="ec70f-141">Quando o valor do campo **ulType** é definido como CONTAB_ROOT, CONTAB_SUBROOT ou CONTAB_CONTAINER, a estrutura do [DIR_ENTRYID](dir_entryid.md) deve ser usada em vez disso.</span><span class="sxs-lookup"><span data-stu-id="ec70f-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ec70f-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec70f-142">See also</span></span>



[<span data-ttu-id="ec70f-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ec70f-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="ec70f-144">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="ec70f-144">MAPI Structures</span></span>](mapi-structures.md)

