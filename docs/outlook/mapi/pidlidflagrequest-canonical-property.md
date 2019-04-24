---
title: Propriedade canônica PidLidFlagRequest
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357803"
---
# <a name="pidlidflagrequest-canonical-property"></a>Propriedade canônica PidLidFlagRequest

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa o status de uma solicitação de reunião.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidRequest  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008530  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Sinalização  <br/> |
   
## <a name="remarks"></a>Comentários

No Microsoft Office Outlook, uma solicitação de reunião é um item de compromisso.
  
Essa propriedade contém um texto que pode ser definido pelo usuário para ser associado ao sinalizador e deve ser definido se o objeto Message estiver sinalizado ou concluído, mas não deve existir para um objeto relacionado à reunião. Os clientes podem optar por não oferecer suporte a essa propriedade e sempre escrever "acompanhamento" (convertido no idioma do usuário, se apropriado) como o valor da cadeia de caracteres quando essa propriedade deve ser definida. Essa propriedade deve ser condicionalmente ignorada com base nos valores das propriedades **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) e **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas à sinalização.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

