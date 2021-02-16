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
ms.openlocfilehash: fba49b052a51bd498f61fc115f630d08fc6c8926
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335793"
---
# <a name="pidtagemsabserver-canonical-property"></a>Propriedade canônica PidTagEmsAbServer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o caminho de um contêiner de catálogo de endereços em um cenário offline ou o nome de domínio totalmente qualificado do servidor de catálogo global onde o contêiner do catálogo de endereços reside em um cenário online.
  
## 

|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W  <br/> |
|Identificador:  <br/> |0xFFFE  <br/> |
|Tipo de dados:  <br/> |PT_TSTRING  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade tem o tipo de propriedade redefinido como **PT_UNICODE** quando ele é compilado com o símbolo em uma plataforma Unicode e para PT_STRING8 quando ele não é compilado com o `UNICODE`  `UNICODE` símbolo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades.
    
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

