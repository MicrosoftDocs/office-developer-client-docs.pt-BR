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
ms.openlocfilehash: 54fe624c98ddb631326853f387372468a61b2f70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770027"
---
# <a name="pidtagservicedllname-canonical-property"></a>Propriedade canônica PidTagServiceDllName

  
  
**Aplica-se a**: Outlook 
  
Contém o nome de arquivo da DLL que contém a função do ponto de entrada do provedor de serviço de mensagem para chamar para configuração.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W  <br/> |
|Identificador:  <br/> |0x3D0A  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Quando o nome de função de ponto de entrada for exibida no método **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), isso indica que o ponto de entrada existe.
  
O MAPI usa uma convenção de nomenclatura de arquivo DLL. O nome do arquivo base contém até seis caracteres que identificam exclusivamente a DLL. MAPI acrescenta a sequência de caracteres 32 como o nome da DLL base para identificar a versão que é executado em plataformas de 32 bits. Por exemplo, quando o nome MAPI. DLL for especificado, o nome MAPI32 construções de MAPI. DLL para representar a versão de 32 bits correspondente da DLL.
  
Essas propriedades devem especificar o nome de base. MAPI acrescenta a sequência de caracteres 32 conforme apropriado. Como parte do resultado propriedades em um erro, incluindo a cadeia de caracteres 32.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

