---
title: Propriedade canônica PidTagDefaultViewEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultViewEntryId
api_type:
- HeaderDef
ms.assetid: 1b4e82ed-c207-4828-8a5b-0ef312962355
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6d284782de86b603e6bbe190931a85cd9196c88b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270011"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>Propriedade canônica PidTagDefaultViewEntryId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o identificador de entrada do modo de exibição padrão de uma pasta.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DEFAULT_VIEW_ENTRYID  <br/> |
|Identificador:  <br/> |0x3616  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é o identificador de entrada do exibição de pasta que deve ser definido como o exibição inicial. A propriedade não precisa ser definida se o modo de exibição "Normal" deve ser usado como o modo de exibição inicial.
  
Um aplicativo cliente pode obter essa propriedade no momento em que abre a pasta e obtém ganhos significativos de desempenho. Essa propriedade pode ser usada como um atalho para obter o modo de exibição padrão, em vez de abrir a tabela de conteúdo associada e enviar uma restrição.
  
Uma implementação de provedor de serviços do [método IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) pode copiar essa propriedade ao copiar pastas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Lida com operações de pasta.
    
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

