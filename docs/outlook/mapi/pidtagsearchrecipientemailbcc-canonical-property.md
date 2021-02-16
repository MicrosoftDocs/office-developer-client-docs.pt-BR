---
title: Propriedade canônica PidTagSearchRecipientEmailBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5b0db4b3bc7903aae74fa7275d3e27e22d628514
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359154"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a>Propriedade canônica PidTagSearchRecipientEmailBcc

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma cadeia de caracteres Unicode que está sendo consultada na lista de endereços de email ou exibe nomes de destinatários endereçados na linha **Cc** de mensagens não enviadas no armazenamento. 
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SEARCH_RECIP_EMAIL_BCC_W  <br/> |
|Identificador:  <br/> |0x0EA8  <br/> |
|Tipo de propriedade:  <br/> |PT_UNICODE  <br/> |
|Acesso:  <br/> |Pesquisa  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade só é relevante para mensagens no armazenamento que não foram enviadas, porque as mensagens que foram enviadas ou recebidas não contêm informações Cc.
  
> [!NOTE]
> Essa marca de restrição MAPI, usada ao pesquisar endereços de email ou exibir nomes para os quais a mensagem será enviada como uma cópia carbono, pode não ser definida no arquivo de título baixável que você tem no momento. Você pode adicioná-lo ao seu código usando o seguinte valor: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`
  
## <a name="related-resources"></a>Recursos relacionados

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

