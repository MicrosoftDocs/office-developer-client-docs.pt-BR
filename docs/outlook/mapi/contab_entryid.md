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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424081"
---
# <a name="contab_entryid"></a><span data-ttu-id="622b2-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="622b2-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="622b2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="622b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="622b2-105">Contém a ID de entrada da pasta de contatos.</span><span class="sxs-lookup"><span data-stu-id="622b2-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="622b2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="622b2-106">Header file:</span></span>  <br/> |<span data-ttu-id="622b2-107">msomapiutil.h</span><span class="sxs-lookup"><span data-stu-id="622b2-107">msomapiutil.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="622b2-108">Members</span><span class="sxs-lookup"><span data-stu-id="622b2-108">Members</span></span>

 <span data-ttu-id="622b2-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="622b2-109">**abFlags**</span></span>
  
> <span data-ttu-id="622b2-110">Uma bitmask de sinalizadores que fornece informações que descrevem o objeto.</span><span class="sxs-lookup"><span data-stu-id="622b2-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="622b2-111">Para obter mais informações, consulte a descrição do **campo abFlags** de uma [estrutura ENTRYID.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="622b2-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="622b2-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="622b2-112">**muid**</span></span>
  
> <span data-ttu-id="622b2-113">GUID que identifica o provedor do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="622b2-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="622b2-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="622b2-114">**ulVersion**</span></span>
  
> <span data-ttu-id="622b2-115">O número da versão da **CONTAB_ENTRYID** estrutura.</span><span class="sxs-lookup"><span data-stu-id="622b2-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="622b2-116">Deve ser definido como CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="622b2-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="622b2-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="622b2-117">**ulType**</span></span>
  
> <span data-ttu-id="622b2-118">Um inteiro que representa o tipo de ID de entrada de contato.</span><span class="sxs-lookup"><span data-stu-id="622b2-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="622b2-119">Deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="622b2-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="622b2-120">**Nome**</span><span class="sxs-lookup"><span data-stu-id="622b2-120">**Name**</span></span>|<span data-ttu-id="622b2-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="622b2-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="622b2-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="622b2-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="622b2-123">Um objeto de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="622b2-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="622b2-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="622b2-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="622b2-125">0" não é um objeto de lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="622b2-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="622b2-126">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="622b2-126">**ulIndex**</span></span>
  
> <span data-ttu-id="622b2-127">O índice no subconjunto de propriedades de email.</span><span class="sxs-lookup"><span data-stu-id="622b2-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="622b2-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="622b2-128">**cbeid**</span></span>
  
> <span data-ttu-id="622b2-129">O tamanho do identificador de entrada da mensagem de contato associada a essa entrada no Address Book de Contatos.</span><span class="sxs-lookup"><span data-stu-id="622b2-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="622b2-130">**abeid**</span><span class="sxs-lookup"><span data-stu-id="622b2-130">**abeid**</span></span>
  
> <span data-ttu-id="622b2-131">O identificador de entrada da mensagem de contato associada a essa entrada no Address Book de Contatos.</span><span class="sxs-lookup"><span data-stu-id="622b2-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="622b2-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="622b2-132">Remarks</span></span>

<span data-ttu-id="622b2-133">Um Address Book de Contatos é um Address Book que contém todos os itens de contato em uma pasta Contatos que têm um endereço de email ou um número de fax.</span><span class="sxs-lookup"><span data-stu-id="622b2-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="622b2-134">Cada entrada em um Address Book de Contatos está associada a um endereço de email ou a um número de fax.</span><span class="sxs-lookup"><span data-stu-id="622b2-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="622b2-135">Como um item de contato pode ter até três endereços de email e três números de fax, um item de contato pode ser representado por até seis entradas no Livro de Endereços de Contatos correspondente.</span><span class="sxs-lookup"><span data-stu-id="622b2-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="622b2-136">O objetivo de um Livro de Endereços de Contatos é dar suporte a usuários endereçamento de mensagens de email para contatos em uma pasta Contatos.</span><span class="sxs-lookup"><span data-stu-id="622b2-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="622b2-137">O provedor do Livro de Endereços de Contatos com suporte do Microsoft Outlook 2010 e do Microsoft Outlook 2013 contab32.dll.</span><span class="sxs-lookup"><span data-stu-id="622b2-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="622b2-138">A **CONTAB_ENTRYID** estrutura suporta um subconjunto das informações presentes na mensagem de Contato MAPI subjacente.</span><span class="sxs-lookup"><span data-stu-id="622b2-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="622b2-139">Ele identifica a mensagem de contato à que uma entrada específica do Livro de Endereços de Contatos está associada.</span><span class="sxs-lookup"><span data-stu-id="622b2-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="622b2-140">Os **campos cbeid** e **abeid** só são válidos quando o valor do campo **ulType** é definido como CONTAB_DISTLIST ou CONTAB_USER.</span><span class="sxs-lookup"><span data-stu-id="622b2-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="622b2-141">Quando o **valor do campo ulType** é definido como CONTAB_ROOT, CONTAB_SUBROOT ou CONTAB_CONTAINER, a estrutura [DIR_ENTRYID](dir_entryid.md) deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="622b2-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="622b2-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="622b2-142">See also</span></span>



[<span data-ttu-id="622b2-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="622b2-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="622b2-144">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="622b2-144">MAPI Structures</span></span>](mapi-structures.md)

