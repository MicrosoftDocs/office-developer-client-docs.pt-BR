---
title: Propriedade canônica PidNameAcceptLanguage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameAcceptLanguage
api_type:
- COM
ms.assetid: 4b202bc1-f718-446a-950f-634ffee47baf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f66a570273d78f63ced110a4bdc8a12a49c531b6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595241"
---
# <a name="pidnameacceptlanguage-canonical-property"></a>Propriedade canônica PidNameAcceptLanguage

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor de campo de cabeçalho [RFC3282] Accept-Language.
  
|||
|:-----|:-----|
|Nomes amigáveis:  <br/> |AcceptLanguage  <br/> |
|Propriedade definida:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nome da propriedade:  <br/> |Idioma aceito  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Comentários

Para definir o valor dessa propriedade, os clientes de mensagem extensões MIME (Multipurpose Internet) devem escrever um campo de cabeçalho Accept-Language com o valor desejado. Clientes MIME podem escrever um campo de cabeçalho de idioma aceitar X em vez disso. Leitores MIME devem copiar o valor de um campo de cabeçalho para o valor dessa propriedade. Se ambos os campos de cabeçalho estiverem presentes, leitores MIME devem usar o campo de cabeçalho Accept-Language.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet para os objetos de mensagem.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

