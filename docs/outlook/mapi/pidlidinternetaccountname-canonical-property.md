---
title: Propriedade canônico de PidLidInternetAccountName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountName
api_type:
- COM
ms.assetid: 29bedadf-903d-419d-804d-dc8bd92b745d
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 6705b121c58e0ff14726f835c779237cb35c32a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768495"
---
# <a name="pidlidinternetaccountname-canonical-property"></a>Propriedade canônico de PidLidInternetAccountName

  
  
**Aplica-se a**: Outlook 
  
Especifica o nome da conta de email do usuário visíveis através do qual a mensagem de email é enviada.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidInetAcctName  <br/> |
|Propriedade definida:  <br/> |PSETID_Common  <br/> |
|ID de longo (LID):  <br/> |0x00008580  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Coment�rios

O formato dessa cadeia de caracteres é dependente de implementação. Essa propriedade pode ser usada pelo cliente para determinar em qual servidor para direcionar o email para, mas é opcional e o valor não tem significado para o servidor.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedade canônico para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md)

