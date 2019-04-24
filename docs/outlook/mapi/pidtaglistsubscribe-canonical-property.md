---
title: Propriedade canônica PidTagListSubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bee11c495d7f1ef21f9af70e6aa89f8c0d0f78b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279654"
---
# <a name="pidtaglistsubscribe-canonical-property"></a>Propriedade canônica PidTagListSubscribe

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o valor de um campo de cabeçalho List-Subscribe da mensagem MIME (Multipurpose Internet Mail Extensions).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W  <br/> |
|Identificador:  <br/> |0x1044  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

Para gerar um campo de cabeçalho de assinatura de lista, os clientes devem definir o valor dessas propriedades para o valor desejado. Os gravadores MIME devem copiar o valor dessas propriedades para o campo de cabeçalho List-Subscribe.
  
Para definir o valor das propriedades relacionadas ao servidor como essas, os clientes MIME devem gravar os campos de cabeçalho conforme especificado na tabela a seguir.
  
|**Property**|**Nome do campo de cabeçalho preferencial**|**Nome do campo de cabeçalho alternativo**|
|:-----|:-----|:-----|
|**PidTagListSubscribe** <br/> |Listar-inscrever  <br/> |X-List-Subscribe  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte as convenções de email padrão da Internet em objetos de mensagem.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

