---
title: Propriedade canônica PidTagRulesTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e1c670cd566e838104ae3d5480c2297f8632d899
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348556"
---
# <a name="pidtagrulestable-canonical-property"></a>Propriedade canônica PidTagRulesTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma tabela com todas as regras aplicadas a uma pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RULES_TABLE  <br/> |
|Identificador:  <br/> |0x3FE1  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Regras no servidor  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade está presente em todos os objetos Folder em um servidor Exchange que tenha regras. Os valores incluídos nessa propriedade são usados para leitura e modificação de regras. Você pode usar o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) com o identificador de interface **IID_IExchangeModifyTable** para obter uma interface [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) para a tabela de regras em uma pasta. Você pode usar essa interface para ler e modificar essas regras. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas. 
    
## <a name="see-also"></a>Confira também



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

