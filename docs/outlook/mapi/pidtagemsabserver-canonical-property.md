---
title: Propriedade canônica PidTagEmsAbServer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0d31272e63df7f68a83b23ca7a3824c081de3c1d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569264"
---
# <a name="pidtagemsabserver-canonical-property"></a>Propriedade canônica PidTagEmsAbServer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o caminho de um contêiner de catálogo de endereços em um cenário offline ou o nome de domínio totalmente qualificado do servidor de catálogo global em que o contêiner de catálogo de endereços reside em um cenário online.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W  <br/> |
|Identificador:  <br/> |0xFFFE  <br/> |
|Tipo de dados:  <br/> |PT_TSTRING  <br/> |
|Área:  <br/> |Catálogo de Endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade tem o tipo de propriedade redefinido com **PT_UNICODE** quando ele é compilado com a `UNICODE` símbolo em uma plataforma de Unicode e **PT_STRING8** quando ele não é compilado com a `UNICODE` símbolo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece as definições do conjunto de propriedades.
    
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

