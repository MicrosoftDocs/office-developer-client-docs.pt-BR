---
title: Propriedade canônica PidTagServiceSupportFiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceSupportFiles
api_type:
- COM
ms.assetid: df4be986-62a8-49d6-8eca-25b55c74f830
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2dc431d807bd74640e5b5a9c020f668b13530197
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770060"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>Propriedade canônica PidTagServiceSupportFiles

  
  
**Aplica-se a**: Outlook 
  
Contém uma lista dos arquivos que pertencem ao serviço de mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W  <br/> |
|Identificador:  <br/> |0x3D0F  <br/> |
|Tipo de dados:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Usando uma caixa de diálogo no miniaplicativo do painel de controle, um usuário pode obter a lista de arquivos que pertencem ao serviço de mensagem. Por exemplo, o usuário pode obter os nomes de todas as bibliotecas de vínculos dinâmicos (DLLs) que pertencem ao serviço. O usuário pode então seek detalhes adicionais sobre os arquivos especificados, como os nomes e números de versão de todas as DLLs. O MAPI usa a essas propriedades para criar uma lista de arquivos de suporte em uma caixa de diálogo para seleção de usuário de mensagens.
  
MAPI funciona somente com nomes de arquivo e outras cadeias de caracteres passada para ele, no conjunto de caracteres do Active Directory Service Interfaces (ANSI). Aplicativos cliente que usam nomes de arquivo em um conjunto de caracteres do fabricante do equipamento original (OEM) devem convertê-los para ANSI antes de chamar MAPI.
  
## <a name="related-resources"></a>Recursos relacionados

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

