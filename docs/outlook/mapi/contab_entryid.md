---
title: CONTAB_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84251222-dac4-4f4d-97b9-aa0e2cd26c44
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 2c8661f24ed9555547446cf63fc08a3be7e6e941
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766305"
---
# <a name="contabentryid"></a>CONTAB_ENTRYID

  
  
**Aplica-se a**: Outlook 
  
Contém a identificação de entrada da pasta Contatos.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |msomapiutil.h  <br/> |
   
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

## <a name="members"></a>Membros

 **abFlags**
  
> Uma bitmask dos sinalizadores que fornece informações que descrevem o objeto. Para obter mais informações, consulte a descrição do campo **abFlags** de uma estrutura de [ENTRYID](entryid.md) . 
    
 **muid**
  
> GUID que identifica o provedor de armazenamento.
    
 **ulVersion**
  
> O número de versão da estrutura **CONTAB_ENTRYID** . Deve ser definida como CONTAB_VERSION. 
    
 **ulType**
  
> Um inteiro que representa o tipo de ID de entrada do contato. Ele deve ser um dos seguintes valores:
    
|**Nome**|**Descrição**|
|:-----|:-----|
|CONTAB_USER  <br/> |Um objeto de usuário de mensagens.  <br/> |
|CONTAB_DISTLIST  <br/> |Um objeto de lista de distribuição.  <br/> |
   
 **ulIndex**
  
> O índice para o subconjunto de propriedade de email.
    
 **cbeid**
  
> O tamanho do identificador de entrada da mensagem de contato associado a essa entrada no catálogo de endereços de contatos.
    
 **abeid**
  
> O identificador de entrada da mensagem de contato associado a essa entrada no catálogo de endereços de contatos.
    
## <a name="remarks"></a>Coment�rios

Um catálogo de endereços de contatos é um catálogo de endereços que contém todos os itens contatos em uma pasta de contatos que têm um endereço de email ou um número de fax. Cada entrada no catálogo de endereços de contatos é associada um endereço de email ou um número de fax. Uma vez que um item de contato pode ter até três endereços de email e três números de fax, um item de contato pode ser representado pela até seis entradas no catálogo de endereços de contatos correspondentes.
  
A finalidade do catálogo de endereços de contatos é suportar usuários lidando com as mensagens de email para contatos em uma pasta Contatos. O provedor de catálogo de endereços de contatos que o Microsoft Outlook 2010 e o Microsoft Outlook 2013 suportam é Contab32.
  
A estrutura **CONTAB_ENTRYID** oferece suporte a um subconjunto das informações que está presentes na mensagem de contato de MAPI subjacente. Identifica a mensagem de contato que uma determinada entrada de catálogo de endereços de contatos está associada. 
  
Os campos **cbeid** e **abeid** são válidos somente quando o valor do campo **ulType** é definido como CONTAB_DISTLIST ou CONTAB_USER. Quando o valor do campo **ulType** é definido como CONTAB_ROOT, CONTAB_SUBROOT ou CONTAB_CONTAINER, a estrutura [DIR_ENTRYID](dir_entryid.md) deve ser usada. 
  
## <a name="see-also"></a>Confira também



[DIR_ENTRYID](dir_entryid.md)


[Estruturas MAPI](mapi-structures.md)

