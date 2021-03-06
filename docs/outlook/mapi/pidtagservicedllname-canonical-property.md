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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330062"
---
# <a name="pidtagservicedllname-canonical-property"></a>Propriedade canônica PidTagServiceDllName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de arquivo da DLL que contém a função de ponto de entrada do provedor de serviços de mensagens a ser chamada para configuração.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W  <br/> |
|Identificador:  <br/> |0x3D0A  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Quando o nome da função de ponto de entrada aparece **no método PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), ele indica que o ponto de entrada existe.
  
MAPI uses a DLL file naming convention. Ele anexa a cadeia de caracteres 32 ao nome base da DLL para identificar a versão que é executado em plataformas de 32 bits. Por exemplo, quando o nome MAPI.DLL especificado, MAPI constrói o nome MAPI32.DLL para representar a versão de 32 bits correspondente da DLL.
  
Essas propriedades devem especificar o nome base. MAPI anexa a cadeia de caracteres 32 conforme apropriado. Incluir a cadeia de caracteres 32 como parte dessas propriedades resulta em um erro.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

