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
ms.openlocfilehash: 3753177552d45e32e53ae192a9dfae15b601afcc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417039"
---
# <a name="pidtagservicesupportfiles-canonical-property"></a>Propriedade canônica PidTagServiceSupportFiles

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista dos arquivos que pertencem ao serviço de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_SUPPORT_FILES, PR_SERVICE_SUPPORT_FILES_A, PR_SERVICE_SUPPORT_FILES_W  <br/> |
|Identificador:  <br/> |0x3D0F  <br/> |
|Tipo de dados:  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Usando uma caixa de diálogo no applet do painel de controle, um usuário pode obter a lista de arquivos que pertencem ao serviço de mensagens. Por exemplo, o usuário pode obter os nomes de todas as bibliotecas de vínculo dinâmico (DLLs) que pertencem ao serviço. Em seguida, o usuário pode procurar detalhes adicionais sobre os arquivos especificados, como os nomes e os números de versão de todas as DLLs. MAPI uses the these properties to create a support file list in a dialog box for messaging user selection.
  
O MAPI funciona somente com nomes de arquivo e outras cadeias de caracteres passadas para ele, no conjunto de caracteres ANSI (Interfaces de Serviço do Active Directory). Os aplicativos cliente que usam nomes de arquivo em um conjunto de caracteres OEM (fabricante de equipamento original) devem convertê-los em ANSI antes de chamar o MAPI.
  
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

