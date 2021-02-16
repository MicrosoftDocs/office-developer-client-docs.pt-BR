---
title: Propriedade canônica PidTagAccessControlListTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424501"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>Propriedade canônica PidTagAccessControlListTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma tabela que consiste em todas as listas de controle de acesso do sistema (SACL) aplicadas a uma pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ACL_TABLE  <br/> |
|Identificador:  <br/> |0x3FE0  <br/> |
|Tipo de dados:  <br/> |PT_OBJECT  <br/> |
|Área:  <br/> |Controle de Acesso  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade está presente em todos os objetos de pasta em um Exchange Server. Os valores incluídos nessa propriedade são usados para ler e modificar listas de controle de acesso (ACLs) em pastas. Você pode usar o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) com o identificador de interface IID_IExchangeModifyTable para obter uma interface [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) para **a** tabela ACL em uma pasta. Você pode usar essa interface para ler e modificar essas ACLs. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

