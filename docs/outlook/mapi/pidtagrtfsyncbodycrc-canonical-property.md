---
title: Propriedade canônica PidTagRtfSyncBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCrc
api_type:
- COM
ms.assetid: 95db4837-400f-476f-b313-60e8baa1c6d1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 85ac61d968243283e5ad9283730941adcd87cd5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357866"
---
# <a name="pidtagrtfsyncbodycrc-canonical-property"></a>Propriedade canônica PidTagRtfSyncBodyCrc

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a verificação de redundância cíclica (CRC) calculada para o texto da mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RTF_SYNC_BODY_CRC  <br/> |
|Identificador:  <br/> |0x1006  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensagem MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

A [função RTFSync](rtfsync.md) calcula o CRC usando apenas os caracteres que considera significativos para a mensagem. Por exemplo, alguns espaços em branco e outros caracteres ignoráveis são omitidos do CRC. 
  
Essa propriedade é uma propriedade auxiliar RTF (Rich Text Format). Essas propriedades são usadas pela **função RTFSync** e não se destinam a ser usadas diretamente por aplicativos cliente. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos de mensagem e anexo para uma representação eficiente de fluxo.
    
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

