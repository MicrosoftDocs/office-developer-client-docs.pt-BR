---
title: Propriedade canônica PidTagReportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReportName
api_type:
- COM
ms.assetid: 4ec3100f-7cf1-4702-b326-e6da586a7bb2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4d3a38f55fa2869df3f8afa1301cf1ad0c7b0737
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769838"
---
# <a name="pidtagreportname-canonical-property"></a>Propriedade canônica PidTagReportName

  
  
**Aplica-se a**: Outlook 
  
Contém o nome de exibição para o destinatário que deve obter relatórios para esta mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_REPORT_NAME, PR_REPORT_NAME_A, PR_REPORT_NAME_W  <br/> |
|Identificador:  <br/> |0x003A  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Envelope MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são exemplos das propriedades de endereço do destinatário que o remetente tenha delegada para receber qualquer relatórios gerados para esta mensagem.
  
Um aplicativo cliente que deve rotear relatórios para outro usuário deve definir essas propriedades em tempo de envio de mensagem. Se não estiver definidas, os relatórios são enviados para o remetente da mensagem.
  
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

