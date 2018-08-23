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
ms.openlocfilehash: 0f65c197999f23d959657cbfee9c6fbb0aaf439f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566282"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a>Propriedade canônica PidTagSearchRecipientEmailBcc

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma cadeia de caracteres Unicode que está sendo consultada na lista de endereços de email ou nomes de exibição dos destinatários abordados na linha **Cco** mensagens não enviadas no repositório. 
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SEARCH_RECIP_EMAIL_BCC_W  <br/> |
|Identificador:  <br/> |0x0EA8  <br/> |
|Tipo de propriedade:  <br/> |PT_UNICODE  <br/> |
|Access:  <br/> |Pesquisar  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade só é relevante para mensagens no repositório que não tem sido enviadas, porque as mensagens que tenham sido enviadas ou recebidas não contêm informações Cco.
  
> [!NOTE]
> Nesta marca de restrição de MAPI, usada durante a pesquisa de endereços de email ou nomes de exibição para o qual a mensagem será enviada como uma cópia carbono oculta, não pode ser definida no arquivo de cabeçalho para download que você possui atualmente. Você pode adicioná-la ao seu código usando o seguinte valor: >`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Microsoft Exchange Server.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

