---
title: Propriedade canônica PidLidOfflineStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418831"
---
# <a name="pidlidofflinestatus-canonical-property"></a>Propriedade canônica PidLidOfflineStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina o estado de um arquivo de documento em um servidor que implementa [MS-LISTSWS].
  
|||
|:-----|:-----|
|Propriedades associadas  <br/> |dispidOfflineStatus  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085B9  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir mostra os valores possíveis dessa propriedade.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |O check-out do documento não foi verificado.  <br/> |
|1   <br/> |Foi verificado o check-out do documento para o usuário atual.  <br/> |
|2   <br/> |O documento não foi verificado, mas o usuário atual tem uma cópia do arquivo salvo para edição no computador atual.  <br/> |
   
Essa propriedade é calculada localmente e não é enviada a um servidor a qualquer momento, a menos que um usuário arraste o item para outra conta. Nesse caso, ele é tratado como uma propriedade personalizada definida pelo usuário.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]] 
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

