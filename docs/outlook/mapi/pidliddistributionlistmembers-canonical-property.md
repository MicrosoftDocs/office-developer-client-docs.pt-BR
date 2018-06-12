---
title: Propriedade canônico de PidLidDistributionListMembers
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c27513474048e9805bc29116aa094bc47f8f0cae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768363"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>Propriedade canônico de PidLidDistributionListMembers

  
  
**Aplica-se a**: Outlook 
  
Especifica a lista de EntryIds dos objetos que correspondem aos membros da lista de distribuição pessoal.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidDLMembers  <br/> |
|Propriedade definida:  <br/> |PSETID_Address  <br/> |
|ID de longo (LID):  <br/> |0x00008055  <br/> |
|Tipo de dados:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Coment�rios

Membros da lista de distribuição pessoal podem ser outras listas de distribuição pessoal, endereços eletrônicos contidos em um contato, os usuários da lista de endereços Global ou listas de distribuição ou endereços de email únicos. O formato de cada EntryId deve ser uma EntryId único, conforme especificado na [[MS-OXCDATA],](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) ou uma EntryId com quebra. 
  
Ao definir essa propriedade, o cliente ou o servidor deve assegurar que seu tamanho total for menor que 15.000 bytes.
  
Essa propriedade especifica a lista de EntryIds únicos que correspondem aos membros da lista de distribuição pessoal. Esses EntryIds únicos encapsulam os nomes para exibição e endereços de email dos membros da lista de distribuição pessoal.
  
Se o cliente ou o servidor definir essa propriedade, ele deve ser sincronizado com esta propriedade **dispidDLMembers** para cada entrada na propriedade **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), deve haver uma entrada no mesma posição no **dispidDLOneOffMembers**.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedade canônico para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md)

