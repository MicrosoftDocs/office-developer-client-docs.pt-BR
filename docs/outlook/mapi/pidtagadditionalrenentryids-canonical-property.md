---
title: Propriedade canônica PidTagAdditionalRenEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIds
api_type:
- HeaderDef
ms.assetid: 8c6e7ca2-1824-4cca-bf69-3c1ea52727de
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4984055d370f3f8ab617b11b2d834ba277ef105a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282358"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a>Propriedade canônica PidTagAdditionalRenEntryIds

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém as identificações de entrada de determinadas pastas especiais. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS  <br/> |
|Identificador:  <br/> |0x36D8  <br/> |
|Tipo de dados:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Aplicativo do Outlook  <br/> |
   
## <a name="remarks"></a>Comentários

As primeiras cinco entradas dessa propriedade de vários valores aplicam-se às seguintes pastas especiais, se existirem no repositório:
  
0-pasta de conflitos
  
1-pasta problemas de sincronização
  
2-pasta falhas locais
  
pasta de falhas de 3 servidores
  
4-pasta de lixo eletrônico
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para criar e localizar as pastas especiais em uma caixa de correio.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifica e marca as mensagens de email que são projetadas para enganar os destinatários para divulgar informações confidenciais (como senhas e outras informações pessoais) para uma fonte não confiável.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação de listas de permissões/bloqueios e a determinação de mensagens de lixo eletrônico.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)


[Sobre a API de Armazenamento](https://msdn.microsoft.com/library/aa192884.aspx)

