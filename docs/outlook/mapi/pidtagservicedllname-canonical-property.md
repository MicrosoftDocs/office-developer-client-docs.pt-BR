---
title: Propriedade canônica PidTagServiceDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 18f3d9462048859fe040e12136ff66f19066764b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2019
ms.locfileid: "31980450"
---
# <a name="pidtagservicedllname-canonical-property"></a>Propriedade canônica PidTagServiceDllName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de arquivo da DLL que contém a função de ponto de entrada do provedor de serviço de mensagens para chamar a configuração.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W  <br/> |
|Identificador:  <br/> |0x3D0A  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Quando o nome da função de ponto de entrada aparece no método **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), ele indica que o ponto de entrada existe.
  
MAPI usa uma Convenção de nomenclatura de arquivo DLL. Ele acrescenta a cadeia de caracteres 32 ao nome da DLL base para identificar a versão que é executada em plataformas de 32 bits. Por exemplo, quando o nome MAPI. DLL for especificado, MAPI cria o nome MAPI32. DLL para representar a versão correspondente de 32 bits da DLL.
  
Essas propriedades devem especificar o nome base. O MAPI anexa a cadeia de caracteres 32 conforme apropriado. Incluir a cadeia de caracteres 32 como parte dessas propriedades resulta em um erro.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

