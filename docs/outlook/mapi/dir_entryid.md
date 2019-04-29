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
# <a name="direntryid"></a>DIR_ENTRYID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve as propriedades de uma ID de entrada de diretório.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |EntryID. h  <br/> |
   
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
  
> Uma bitmask de sinalizadores que fornece informações que descrevem o objeto. Para obter mais informações, consulte a descrição do campo **abFlags** de uma estrutura [EntryID](entryid.md) . 
    
 **muid**
  
> GUID que identifica o provedor de repositório.
    
 **ulVersion**
  
> O número da versão da estrutura **DIR_ENTRYID** . Deve ser definido como CONTAB_VERSION. 
    
 **ulType**
  
> Um inteiro que representa o tipo de ID de entrada de diretório. Deve ser um dos seguintes valores:
    
|**Nome**|**Descrição**|
|:-----|:-----|
|CONTAB_ROOT  <br/> |A pasta raiz de um catálogo de endereços MAPI.  <br/> |
|CONTAB_SUBROOT  <br/> |Uma subpasta contida na pasta raiz do objeto de catálogos de endereços MAPI.  <br/> |
|CONTAB_CONTAINER  <br/> |Abrir o contêiner de um objeto do catálogo de endereços.  <br/> |
   
 **muidID**
  
> Um GUID que identifica o objeto de logon.
    
## <a name="remarks"></a>Comentários

As estruturas **DIR_ENTRYID** e [CONTAB_ENTRYID](contab_entryid.md) são idênticas, exceto para o membro **ulType** . O conteúdo do membro **ulType** determina qual estrutura é adequada para os campos restantes. 
  
## <a name="see-also"></a>Confira também



[CONTAB_ENTRYID](contab_entryid.md)


[Estruturas MAPI](mapi-structures.md)

