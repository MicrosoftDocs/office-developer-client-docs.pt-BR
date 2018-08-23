---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3307bb252ca4436999a541f85657fed9878c798a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579393"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um controle de lista suspensa que será usado em uma caixa de diálogo construída a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a>Members

 **ulFlags**
  
> Reservado, deve ser zero. 
    
 **ulPRDisplayProperty**
  
> Marca de propriedade para uma propriedade do tipo PT_TSTRING. Essa propriedade é uma das colunas na tabela identificado pelo membro **ulPRTableName** . Os valores para essa propriedade são exibidos na lista. 
    
 **ulPRSetProperty**
  
> Marca de propriedade para uma propriedade de qualquer tipo. Essa propriedade é uma das colunas na tabela identificado pelo membro **ulPRTableName** . Quando o usuário da lista Selecionar um valor de propriedade para o membro **ulPRDisplayProperty** das linhas da tabela identificado pelo membro **ulPRTableName** , o membro **ulPRSetProperty** correspondente é definido. 
    
 **ulPRTableName**
  
> Marca de propriedade para uma propriedade de tabela do tipo PT_OBJECT que podem ser abertos usando uma **OpenProperty** chamar. A tabela deve ter duas colunas: **ulPRDisplayProperty** e **ulPRSetProperty**. As linhas da tabela devem corresponder ao itens na lista.
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLDDLBX** descreve um controle de lista suspensa que é exibido como um único item, até que o usuário escolhe expandi-la. 
  
As três propriedades identificadas pelas marcas de propriedade trabalham juntos para exibir as informações na lista e definir uma propriedade relacionada. O membro **ulPRTableName** é um objeto table que é acessado por meio de uma chamada para [IMAPIProp::OpenProperty](imapiprop-openproperty.md). A tabela tem duas colunas: uma coluna para a propriedade identificada pelo membro **ulPRDisplayProperty** e outro para a propriedade identificada pelo membro **ulPRSetProperty** . 
  
A propriedade **ulPRDisplayProperty** controla a exibição de lista. Quando o usuário seleciona um dos valores da exibição, chamadas de MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) para definir a propriedade correspondente, conforme identificado pelo membro **ulPRSetProperty** . Isso significa que a propriedade na mesma linha como a propriedade de exibição selecionado. O membro **ulPRSetProperty** não pode ser definido como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
  
Um valor inicial será exibido na lista, se tiver recuperado a propriedade representada pelo membro **ulPRSetProperty** por meio de uma chamada para [IMAPIProp::GetProps](imapiprop-getprops.md) e localizada uma linha na tabela com o valor para o membro **ulPRSetProperty** MAPI. O valor exibido inicial é o conteúdo da coluna **ulPRDisplayProperty** daquela que corresponda a propriedade no membro **ulPRDisplayProperty** da estrutura de linha. O valor retornado pela **GetProps** para a propriedade identificada pelo membro **ulPRDisplayProperty** torna-se o valor inicial que é exibido quando a lista é exibida primeiro. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md). Para obter informações sobre os tipos de propriedade, consulte [Visão geral do tipo de propriedade de MAPI](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[Estruturas MAPI](mapi-structures.md)
  
[Implementação da tabela de exibição](display-table-implementation.md)
  
[Exibir tabelas](display-tables.md)
  
[Visão geral do tipo de propriedade MAPI](mapi-property-type-overview.md)

