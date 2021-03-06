---
title: Propriedade canônica PidLidDistributionListMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335067"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>Propriedade canônica PidLidDistributionListMembers

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica a lista de EntryIds dos objetos que correspondem aos membros da lista de distribuição pessoal.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidDLMembers  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008055  <br/> |
|Tipo de dados:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Comentários

Os membros da lista de distribuição pessoal podem ser outras listas de distribuição pessoais, endereços eletrônicos contidos em um contato, usuários ou listas de distribuição da Lista de Endereços Global ou endereços de email único. O formato de cada EntryId deve ser uma EntryId única, conforme especificado em [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) ou uma EntryId empacotada. 
  
Ao definir essa propriedade, o cliente ou o servidor deve garantir que seu tamanho total seja inferior a 15.000 bytes.
  
Esta propriedade especifica a lista de EntryIds que correspondem aos membros da lista de distribuição pessoal. Esses EntryIds one-off encapsulam nomes de exibição e endereços de email dos membros da lista de distribuição pessoal.
  
Se o cliente ou o servidor definir essa propriedade, ela deverá ser sincronizada com essa propriedade **dispidDLMembers** para cada entrada na **propriedade dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), deve haver uma entrada na mesma posição na **dispidDLOneOffMembers**.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

