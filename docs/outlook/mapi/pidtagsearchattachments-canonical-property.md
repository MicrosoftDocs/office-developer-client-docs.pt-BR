---
title: Propriedade canônica PidTagSearchAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 008dd69f5e31b601b678a4346880e6b3c89a0f39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769976"
---
# <a name="pidtagsearchattachments-canonical-property"></a>Propriedade canônica PidTagSearchAttachments

  
  
**Aplica-se a**: Outlook 
  
Contém uma cadeia de caracteres Unicode que está sendo consultada no conteúdo de anexo no repositório.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SEARCH_ATTACHMENTS_W  <br/> |
|Identificador:  <br/> |0x0EA5  <br/> |
|Tipo de propriedade:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Pesquisar  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

> [!NOTE]
> Nesta marca de restrição de MAPI, usada quando você estiver procurando por conteúdo de anexo, não poderão ser definida no arquivo de cabeçalho para download que você possui atualmente. Você pode adicioná-la ao seu código usando o seguinte valor: >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`
  
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

