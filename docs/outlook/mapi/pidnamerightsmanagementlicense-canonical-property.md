---
title: Propriedade canônica PidNameRightsManagementLicense
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameRightsManagementLicense
api_type:
- COM
ms.assetid: ca3c9317-7873-4f37-b78f-b35467c81c29
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 889b823a55c39ebc19e52c8cc9a1d078a5732a01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315019"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a>Propriedade canônica PidNameRightsManagementLicense

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Armazena em cache a licença de uso da mensagem de email gerenciada por direitos.
  
|||
|:-----|:-----|
|Nomes amigáveis:  <br/> |Nenhum  <br/> |
|Conjunto de propriedades:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Nome da propriedade:  <br/> |DRMLicense  <br/> |
|Tipo de dados:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Mensagens seguras  <br/> |
   
## <a name="remarks"></a>Comentários

Se a propriedade estiver presente em uma mensagem de email gerenciada por direitos, o primeiro valor dessa propriedade Binary Multiple deverá conter o ZLIB (conforme especificado em [RFC1950]) licença de uso compactada para a mensagem de email gerenciada por direitos.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica as propriedades de mensagens codificadas por direitos gerenciados.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

