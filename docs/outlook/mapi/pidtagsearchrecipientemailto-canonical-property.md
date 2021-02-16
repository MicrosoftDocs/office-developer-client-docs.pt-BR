---
title: Propriedade canônica PidTagSearchRecipientEmailTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d254df132db5542ce5235c1c3ab42ea768399f0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358916"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a>Propriedade canônica PidTagSearchRecipientEmailTo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma cadeia de caracteres Unicode que está sendo consultada na lista  de endereços de email ou exibe nomes de destinatários endereçados na linha Para de mensagens no armazenamento. 
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SEARCH_RECIP_EMAIL_TO_W  <br/> |
|Identificador:  <br/> |0x0EA6  <br/> |
|Tipo de propriedade:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Pesquisa  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

> [!NOTE]
> Essa marca de restrição MAPI, usada quando você pesquisa endereços de email ou exibe nomes para os quais a mensagem é enviada, pode não ser definida no arquivo de título baixável que você tem no momento. Você pode adicioná-lo ao seu código usando o seguinte valor: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`
  
### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo do Microsoft Exchange Server relacionadas.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

