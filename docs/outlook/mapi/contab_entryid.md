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
ms.openlocfilehash: ff088dc5bf62f407692c9eec649ff388f79d549d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567150"
---
# <a name="contabentryid"></a><span data-ttu-id="679db-103">CONTAB_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="679db-103">CONTAB_ENTRYID</span></span>

  
  
<span data-ttu-id="679db-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="679db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="679db-105">Contém a identificação de entrada da pasta Contatos.</span><span class="sxs-lookup"><span data-stu-id="679db-105">Contains the entry ID of the contacts folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="679db-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="679db-106">Header file:</span></span>  <br/> |<span data-ttu-id="679db-107">msomapiutil.h</span><span class="sxs-lookup"><span data-stu-id="679db-107">msomapiutil.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="679db-108">Members</span><span class="sxs-lookup"><span data-stu-id="679db-108">Members</span></span>

 <span data-ttu-id="679db-109">**abFlags**</span><span class="sxs-lookup"><span data-stu-id="679db-109">**abFlags**</span></span>
  
> <span data-ttu-id="679db-110">Uma bitmask dos sinalizadores que fornece informações que descrevem o objeto.</span><span class="sxs-lookup"><span data-stu-id="679db-110">A bitmask of flags that provides information describing the object.</span></span> <span data-ttu-id="679db-111">Para obter mais informações, consulte a descrição do campo **abFlags** de uma estrutura de [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="679db-111">For more information, see the description of the **abFlags** field of an [ENTRYID](entryid.md) structure.</span></span> 
    
 <span data-ttu-id="679db-112">**muid**</span><span class="sxs-lookup"><span data-stu-id="679db-112">**muid**</span></span>
  
> <span data-ttu-id="679db-113">GUID que identifica o provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="679db-113">GUID that identifies the store provider.</span></span>
    
 <span data-ttu-id="679db-114">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="679db-114">**ulVersion**</span></span>
  
> <span data-ttu-id="679db-115">O número de versão da estrutura **CONTAB_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="679db-115">The version number of the **CONTAB_ENTRYID** structure.</span></span> <span data-ttu-id="679db-116">Deve ser definida como CONTAB_VERSION.</span><span class="sxs-lookup"><span data-stu-id="679db-116">Must be set to CONTAB_VERSION.</span></span> 
    
 <span data-ttu-id="679db-117">**ulType**</span><span class="sxs-lookup"><span data-stu-id="679db-117">**ulType**</span></span>
  
> <span data-ttu-id="679db-118">Um inteiro que representa o tipo de ID de entrada do contato.</span><span class="sxs-lookup"><span data-stu-id="679db-118">An integer representing the contact entry ID type.</span></span> <span data-ttu-id="679db-119">Ele deve ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="679db-119">It must be one of the following values:</span></span>
    
|<span data-ttu-id="679db-120">**Nome**</span><span class="sxs-lookup"><span data-stu-id="679db-120">**Name**</span></span>|<span data-ttu-id="679db-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="679db-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="679db-122">CONTAB_USER</span><span class="sxs-lookup"><span data-stu-id="679db-122">CONTAB_USER</span></span>  <br/> |<span data-ttu-id="679db-123">Um objeto de usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="679db-123">A messaging user object.</span></span>  <br/> |
|<span data-ttu-id="679db-124">CONTAB_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="679db-124">CONTAB_DISTLIST</span></span>  <br/> |<span data-ttu-id="679db-125">Um objeto de lista de distribuição.</span><span class="sxs-lookup"><span data-stu-id="679db-125">A distribution list object.</span></span>  <br/> |
   
 <span data-ttu-id="679db-126">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="679db-126">**ulIndex**</span></span>
  
> <span data-ttu-id="679db-127">O índice para o subconjunto de propriedade de email.</span><span class="sxs-lookup"><span data-stu-id="679db-127">The index into the email property subset.</span></span>
    
 <span data-ttu-id="679db-128">**cbeid**</span><span class="sxs-lookup"><span data-stu-id="679db-128">**cbeid**</span></span>
  
> <span data-ttu-id="679db-129">O tamanho do identificador de entrada da mensagem de contato associado a essa entrada no catálogo de endereços de contatos.</span><span class="sxs-lookup"><span data-stu-id="679db-129">The size of the entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
 <span data-ttu-id="679db-130">**abeid**</span><span class="sxs-lookup"><span data-stu-id="679db-130">**abeid**</span></span>
  
> <span data-ttu-id="679db-131">O identificador de entrada da mensagem de contato associado a essa entrada no catálogo de endereços de contatos.</span><span class="sxs-lookup"><span data-stu-id="679db-131">The entry identifier of the Contact message associated with this entry in the Contacts Address Book.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="679db-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="679db-132">Remarks</span></span>

<span data-ttu-id="679db-133">Um catálogo de endereços de contatos é um catálogo de endereços que contém todos os itens contatos em uma pasta de contatos que têm um endereço de email ou um número de fax.</span><span class="sxs-lookup"><span data-stu-id="679db-133">A Contacts Address Book is an Address Book that contains all the contact items in a Contacts folder that have either an email address or a fax number.</span></span> <span data-ttu-id="679db-134">Cada entrada no catálogo de endereços de contatos é associada um endereço de email ou um número de fax.</span><span class="sxs-lookup"><span data-stu-id="679db-134">Each entry in a Contacts Address Book is associated with either an email address or a fax number.</span></span> <span data-ttu-id="679db-135">Uma vez que um item de contato pode ter até três endereços de email e três números de fax, um item de contato pode ser representado pela até seis entradas no catálogo de endereços de contatos correspondentes.</span><span class="sxs-lookup"><span data-stu-id="679db-135">Since a contact item can have up to three email addresses and three fax numbers, a contact item can be represented by up to six entries in the corresponding Contacts Address Book.</span></span>
  
<span data-ttu-id="679db-136">A finalidade do catálogo de endereços de contatos é suportar usuários lidando com as mensagens de email para contatos em uma pasta Contatos.</span><span class="sxs-lookup"><span data-stu-id="679db-136">The purpose of a Contacts Address Book is to support users addressing email messages to contacts in a Contacts folder.</span></span> <span data-ttu-id="679db-137">O provedor de catálogo de endereços de contatos que o Microsoft Outlook 2010 e o Microsoft Outlook 2013 suportam é Contab32.</span><span class="sxs-lookup"><span data-stu-id="679db-137">The Contacts Address Book provider that Microsoft Outlook 2010 and Microsoft Outlook 2013 support is contab32.dll.</span></span>
  
<span data-ttu-id="679db-138">A estrutura **CONTAB_ENTRYID** oferece suporte a um subconjunto das informações que está presentes na mensagem de contato de MAPI subjacente.</span><span class="sxs-lookup"><span data-stu-id="679db-138">The **CONTAB_ENTRYID** structure supports a subset of the information that is present in the underlying MAPI Contact message.</span></span> <span data-ttu-id="679db-139">Identifica a mensagem de contato que uma determinada entrada de catálogo de endereços de contatos está associada.</span><span class="sxs-lookup"><span data-stu-id="679db-139">It identifies the Contact message that a particular Contacts Address Book entry is associated with.</span></span> 
  
<span data-ttu-id="679db-140">Os campos **cbeid** e **abeid** são válidos somente quando o valor do campo **ulType** é definido como CONTAB_DISTLIST ou CONTAB_USER.</span><span class="sxs-lookup"><span data-stu-id="679db-140">The **cbeid** and **abeid** fields are only valid when the **ulType** field value is set to CONTAB_DISTLIST or CONTAB_USER.</span></span> <span data-ttu-id="679db-141">Quando o valor do campo **ulType** é definido como CONTAB_ROOT, CONTAB_SUBROOT ou CONTAB_CONTAINER, a estrutura [DIR_ENTRYID](dir_entryid.md) deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="679db-141">When the **ulType** field value is set to CONTAB_ROOT, CONTAB_SUBROOT, or CONTAB_CONTAINER, the [DIR_ENTRYID](dir_entryid.md) structure should be used instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="679db-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="679db-142">See also</span></span>



[<span data-ttu-id="679db-143">DIR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="679db-143">DIR_ENTRYID</span></span>](dir_entryid.md)


[<span data-ttu-id="679db-144">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="679db-144">MAPI Structures</span></span>](mapi-structures.md)

