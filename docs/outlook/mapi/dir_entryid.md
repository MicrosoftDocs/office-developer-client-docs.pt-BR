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
# <a name="direntryid"></a>DIR_ENTRYID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve as propriedades de uma identificação de entrada de diretório.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |EntryID.h  <br/> |
   
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

## <a name="members"></a>Members

 **abFlags**
  
> Uma bitmask dos sinalizadores que fornece informações que descrevem o objeto. Para obter mais informações, consulte a descrição do campo **abFlags** de uma estrutura de [ENTRYID](entryid.md) . 
    
 **muid**
  
> GUID que identifica o provedor de armazenamento.
    
 **ulVersion**
  
> O número de versão da estrutura **DIR_ENTRYID** . Deve ser definida como CONTAB_VERSION. 
    
 **ulType**
  
> Um inteiro que representa o tipo de ID de entrada de diretório. Ele deve ser um dos seguintes valores:
    
|**Nome**|**Descrição**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |A pasta raiz de um catálogo de endereços MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |Uma subpasta contida na pasta raiz do objeto de catálogo de endereços MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |Um objeto de contêiner de catálogo de endereços.  <br/> |
   
 **muidID**
  
> Um GUID que identifica o objeto de logon.
    
## <a name="remarks"></a>Comentários

As estruturas **DIR_ENTRYID** e [CONTAB_ENTRYID](contab_entryid.md) são idênticas, exceto para o membro **ulType** . O conteúdo do membro **ulType** determinar qual estrutura é apropriada para os campos restantes. 
  
## <a name="see-also"></a>Confira também



[CONTAB_ENTRYID](contab_entryid.md)


[Estruturas MAPI](mapi-structures.md)

