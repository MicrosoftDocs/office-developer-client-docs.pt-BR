---
title: Propriedade canônica PidTagProviderDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286485"
---
# <a name="pidtagproviderdllname-canonical-property"></a>Propriedade canônica PidTagProviderDllName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de arquivo base da biblioteca de vínculo dinâmico (DLL) do provedor de serviços MAPI.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W  <br/> |
|Identificador:  <br/> |0x300A  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |MAPI comum  <br/> |
   
## <a name="remarks"></a>Comentários

MAPI uses a DLL file naming convention. Ele anexa a cadeia de caracteres 32 ao nome base da DLL para identificar a versão que é executado em plataformas de 32 bits. Por exemplo, quando o nome MAPI.DLL especificado, MAPI constrói o nome MAPI32.DLL para representar a versão de 32 bits correspondente da DLL.
  
Essas propriedades devem especificar o nome base. MAPI anexa a cadeia de caracteres 32 conforme apropriado. Incluir a cadeia de caracteres 32 como parte dessa propriedade resulta em um erro.
  
## <a name="related-resources"></a>Recursos relacionados

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

