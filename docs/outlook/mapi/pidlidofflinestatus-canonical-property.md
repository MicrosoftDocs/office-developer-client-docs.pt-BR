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
ms.openlocfilehash: 7d9f8cf4fbdeab70e40447411ed8efd35ef7899e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588773"
---
# <a name="pidlidofflinestatus-canonical-property"></a>Propriedade canônica PidLidOfflineStatus

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina o estado de um arquivo de documento em um servidor que implementa [MS-LISTSWS].
  
|||
|:-----|:-----|
|Propriedades associadas  <br/> |dispidOfflineStatus  <br/> |
|Propriedade definida:  <br/> |PSETID_Common  <br/> |
|ID de longo (LID):  <br/> |0x000085B9  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

A tabela a seguir mostra os possíveis valores dessa propriedade.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0  <br/> |Documento não está com check-out.  <br/> |
|1  <br/> |Documento está com check-out para o usuário atual.  <br/> |
|2  <br/> |Documento não está com check-out, mas o usuário atual tem uma cópia do arquivo salvo para edição no computador atual.  <br/> |
   
Essa propriedade é calculada localmente e não é enviada para um servidor a qualquer momento, a menos que um usuário arrasta o item para outra conta. Nesse caso, ela será tratada como uma propriedade personalizada definida pelo usuário.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]] 
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

