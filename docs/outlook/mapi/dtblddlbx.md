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
ms.openlocfilehash: 244aaea4902d6be8eda4cdca176436af9b002ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438845"
---
# <a name="dtblddlbx"></a>DTBLDDLBX

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve um controle de lista drop-down que será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
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

## <a name="members"></a>Membros

 **ulFlags**
  
> Reservado, deve ser zero. 
    
 **ulPRDisplayProperty**
  
> Marca de propriedade de uma propriedade do tipo PT_TSTRING. Essa propriedade é uma das colunas na tabela identificada pelo **membro ulPRTableName.** Os valores dessa propriedade são exibidos na lista. 
    
 **ulPRSetProperty**
  
> Marca de propriedade para uma propriedade de qualquer tipo. Essa propriedade é uma das colunas na tabela identificada pelo **membro ulPRTableName.** Quando o usuário da lista seleciona um valor de propriedade para o membro **ulPRDisplayProperty** das linhas da tabela identificada pelo membro **ulPRTableName,** o membro **ulPRSetProperty** correspondente é definido. 
    
 **ulPRTableName**
  
> Marca de propriedade de uma propriedade de tabela do tipo PT_OBJECT que pode ser aberta usando uma **chamada OpenProperty.** A tabela deve ter duas colunas: **ulPRDisplayProperty** e **ulPRSetProperty**. As linhas da tabela devem corresponder aos itens na lista.
    
## <a name="remarks"></a>Comentários

Uma **estrutura DTBLDDLBX** descreve um controle de lista drop-down que é exibido como um único item até que o usuário opte por expandi-lo. 
  
As três propriedades identificadas pelas marcas de propriedade funcionam juntas para exibir as informações na lista e definir uma propriedade relacionada. O **membro ulPRTableName** é um objeto de tabela que é acessado por meio de uma chamada para [IMAPIProp::OpenProperty](imapiprop-openproperty.md). A tabela tem duas colunas: uma coluna para a propriedade identificada pelo membro **ulPRDisplayProperty** e a outra para a propriedade identificada pelo **membro ulPRSetProperty.** 
  
A **propriedade ulPRDisplayProperty** orienta a exibição da lista. Quando um usuário seleciona um dos valores na exibição, MAPI chama [IMAPIProp::SetProps](imapiprop-setprops.md) para definir a propriedade correspondente conforme identificado pelo **membro ulPRSetProperty.** Isso significa que a propriedade na mesma linha que a propriedade de exibição selecionada. O **membro ulPRSetProperty** não pode ser definido como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
  
Um valor inicial será exibido na lista se MAPI tiver recuperado a propriedade representada pelo membro **ulPRSetProperty** por meio de uma chamada para [IMAPIProp::GetProps](imapiprop-getprops.md) e localizado uma linha na tabela com o valor do membro **ulPRSetProperty.** O valor exibido inicial é o conteúdo da coluna **ulPRDisplayProperty** dessa linha que corresponde à propriedade no **membro ulPRDisplayProperty** da estrutura. O valor retornado por **GetProps** para a propriedade identificada pelo membro **ulPRDisplayProperty** torna-se o valor inicial mostrado quando a lista é exibida pela primeira vez. 
  
Para uma visão geral das tabelas de exibição, consulte [Display Tables](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela de exibição.](display-table-implementation.md) Para obter informações sobre tipos de propriedade, consulte [Visão geral do tipo de propriedade MAPI.](mapi-property-type-overview.md)
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)


[Estruturas MAPI](mapi-structures.md)
  
[Implementação da tabela de exibição](display-table-implementation.md)
  
[Exibir Tabelas](display-tables.md)
  
[Visão geral do tipo de propriedade MAPI](mapi-property-type-overview.md)

