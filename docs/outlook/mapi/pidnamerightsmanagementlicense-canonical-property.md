---
title: Propriedade canônico de PidNameRightsManagementLicense
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c75cb480b9a1a7ffdcff9c0f9b49aabba746fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768864"
---
# <a name="pidnamerightsmanagementlicense-canonical-property"></a>Propriedade canônico de PidNameRightsManagementLicense

  
  
**Aplica-se a**: Outlook 
  
Armazena em cache a licença de uso para a mensagem de email gerenciadas por direitos.
  
|||
|:-----|:-----|
|Nomes amigáveis:  <br/> |None  <br/> |
|Propriedade definida:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Nome da propriedade:  <br/> |DRMLicense  <br/> |
|Tipo de dados:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Mensagens seguras  <br/> |
   
## <a name="remarks"></a>Coment�rios

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
  
[Mapear nomes de propriedade canônico para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md)

