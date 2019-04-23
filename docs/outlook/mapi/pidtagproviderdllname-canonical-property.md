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
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980452"
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

MAPI usa uma Convenção de nomenclatura de arquivo DLL. Ele acrescenta a cadeia de caracteres 32 ao nome da DLL base para identificar a versão que é executada em plataformas de 32 bits. Por exemplo, quando o nome MAPI. DLL for especificado, MAPI cria o nome MAPI32. DLL para representar a versão correspondente de 32 bits da DLL.
  
Essas propriedades devem especificar o nome base. O MAPI anexa a cadeia de caracteres 32 conforme apropriado. Incluir a cadeia de caracteres 32 como parte dessa propriedade resulta em um erro.
  
## <a name="related-resources"></a>Recursos relacionados

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

