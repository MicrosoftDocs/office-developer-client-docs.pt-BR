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
# <a name="contabentryid"></a>CONTAB_ENTRYID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a identificação de entrada da pasta contatos.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |msomapiutil. h  <br/> |
   
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

## <a name="members"></a>Members

 **abFlags**
  
> Uma bitmask de sinalizadores que fornece informações que descrevem o objeto. Para obter mais informações, consulte a descrição do campo **abFlags** de uma estrutura [EntryID](entryid.md) . 
    
 **muid**
  
> GUID que identifica o provedor de repositório.
    
 **ulVersion**
  
> O número da versão da estrutura **CONTAB_ENTRYID** . Deve ser definido como CONTAB_VERSION. 
    
 **ulType**
  
> Um inteiro que representa o tipo de ID de entrada de contato. Deve ser um dos seguintes valores:
    
|**Nome**|**Descrição**|
|:-----|:-----|
|CONTAB_USER  <br/> |Um objeto de usuário de mensagens.  <br/> |
|CONTAB_DISTLIST  <br/> |0" não é um objeto de lista de distribuição.  <br/> |
   
 **ulIndex**
  
> O índice do subconjunto de propriedades de email.
    
 **cbeid**
  
> O tamanho do identificador de entrada da mensagem de contato associada a essa entrada no catálogo de endereços de contatos.
    
 **Abeid**
  
> O identificador de entrada da mensagem de contato associada a essa entrada no catálogo de endereços de contatos.
    
## <a name="remarks"></a>Comentários

Um catálogo de endereços de contatos é um catálogo de endereços que contém todos os itens de contato em uma pasta de contatos que tem um endereço de email ou um número de fax. Cada entrada em um catálogo de endereços de contatos é associada a um endereço de email ou a um número de fax. Como um item de contato pode ter até três endereços de email e três números de fax, um item de contato pode ser representado por até seis entradas no catálogo de endereços de contatos correspondente.
  
O objetivo de um catálogo de endereços de contatos é oferecer suporte aos usuários que endereçam mensagens de email para contatos em uma pasta de contatos. O provedor de catálogo de endereços de contatos que o Microsoft Outlook 2010 e o Microsoft Outlook 2013 oferecem suporte é contab32. dll.
  
A estrutura **CONTAB_ENTRYID** oferece suporte a um subconjunto das informações presentes na mensagem de contato MAPI subjacente. Ele identifica a mensagem de contato à qual uma entrada de catálogo de endereços de contatos específica está associada. 
  
Os campos **cbeid** e **Abeid** são válidos somente quando o valor do campo **ulType** é definido como CONTAB_DISTLIST ou CONTAB_USER. Quando o valor do campo **ulType** é definido como CONTAB_ROOT, CONTAB_SUBROOT ou CONTAB_CONTAINER, a estrutura do [DIR_ENTRYID](dir_entryid.md) deve ser usada em vez disso. 
  
## <a name="see-also"></a>Confira também



[DIR_ENTRYID](dir_entryid.md)


[Estruturas MAPI](mapi-structures.md)

