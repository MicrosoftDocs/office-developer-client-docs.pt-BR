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
ms.openlocfilehash: 1f528332c52664ac472670566c905d36dac65bfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565526"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a>Propriedade canônica PidNameRightsManagementLicense

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Armazena em cache a licença de uso para a mensagem de email gerenciadas por direitos.
  
|||
|:-----|:-----|
|Nomes amigáveis:  <br/> |Nenhum  <br/> |
|Propriedade definida:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Nome da propriedade:  <br/> |DRMLicense  <br/> |
|Tipo de dados:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Mensagens seguras  <br/> |
   
## <a name="remarks"></a>Comentários

Se a propriedade estiver presente em uma mensagem de email gerenciadas por direitos, o primeiro valor dessa propriedade binário vários deve conter a licença de uso compactado ZLIB (conforme especificado em [RFC1950]) para a mensagem de email gerenciadas por direitos.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica as propriedades das mensagens codificadas direitos gerenciados.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

