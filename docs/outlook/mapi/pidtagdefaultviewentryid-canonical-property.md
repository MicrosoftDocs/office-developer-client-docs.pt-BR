---
title: Propriedade canônica PidTagDefaultViewEntryId Canonical
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
ms.openlocfilehash: 2c941ea43a19b51e46c00b37aa89f504c55f180a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587205"
---
# <a name="pidtagdefaultviewentryid-canonical-property"></a>Propriedade canônica PidTagDefaultViewEntryId Canonical

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o identificador de entrada do modo de exibição da pasta padrão.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DEFAULT_VIEW_ENTRYID  <br/> |
|Identificador:  <br/> |0x3616  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Contêiner MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é o identificador de entrada da exibição da pasta que deve ser definido como o modo de exibição inicial. A propriedade não precisa ser definida se o modo de exibição do "Normal" deve ser usado como o modo de exibição inicial.
  
Um aplicativo cliente pode obter esta propriedade no momento em que ele abre a pasta e concretizar ganhos significativos de desempenho. Esta propriedade pode ser usada como um atalho para obter o modo de exibição padrão, em vez de abrir a tabela de conteúdo associado e o envio de uma restrição.
  
Uma implementação do provedor de serviço do método [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md) pode copiar essa propriedade quando ele copia pastas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Trata as operações de pasta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

