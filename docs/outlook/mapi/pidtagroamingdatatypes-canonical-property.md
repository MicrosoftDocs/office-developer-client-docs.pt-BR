---
title: Propriedade canônica PidTagRoamingDatatypes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359553"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a>Propriedade canônica PidTagRoamingDatatypes

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma máscara de bits que indica quais propriedades de fluxo existem na mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ROAMING_DATATYPES  <br/> |
|Identificador:  <br/> |0x7C06  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Configuração  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade deve ser definida como um ou mais dos seguintes valores:
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0x00000002  <br/> |Indica que a mensagem FAI (Informações Associadas à Pasta) deve conter um fluxo de dicionário, serializado em um esquema XML fixo e armazenado na propriedade **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)). Se a mensagem fai não contém um fluxo de dicionário, o aplicativo deve tratar o dicionário como não tendo entradas.  <br/> |
|0x00000004  <br/> |Indica que a mensagem FAI deve conter um fluxo XML armazenado na propriedade **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) que usa um esquema XML arbitrário.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Especifica o local e as propriedades dos dados de configuração do cliente e do servidor, como listas de categorias compartilhadas e horas de trabalho.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

