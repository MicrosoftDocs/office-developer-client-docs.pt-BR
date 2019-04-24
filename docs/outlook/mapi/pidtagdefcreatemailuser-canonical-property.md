---
title: Propriedade canônica PidTagDefCreateMailuser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cd09c85e4f44bbea29807d72a273ccf6980ca6df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269983"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a>Propriedade canônica PidTagDefCreateMailuser

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o identificador de entrada de modelo para um objeto de usuário de mensagem padrão. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DEF_CREATE_MAILUSER  <br/> |
|Identificador:  <br/> |0x3612  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Os aplicativos cliente usam essa propriedade para criar um objeto de usuário de mensagens dentro de um contêiner. O suporte à criação de entrada é opcional para contêineres do catálogo de endereços; os que não oferecem suporte a ele não são necessários para expor essa propriedade. 
  
Esta propriedade especifica uma entrada que pode aparecer na propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para usuários de mensagens. Após obter o identificador, o cliente o usará em uma chamada para o método [IABContainer:: createentry](iabcontainer-createentry.md) . A entrada representa o modelo do usuário de mensagens padrão. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

