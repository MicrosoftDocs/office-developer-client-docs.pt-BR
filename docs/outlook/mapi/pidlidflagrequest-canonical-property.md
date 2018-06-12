---
title: Propriedade canônico de PidLidFlagRequest
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: df2e474206559dadf250bdf9a078c69da61187c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768466"
---
# <a name="pidlidflagrequest-canonical-property"></a>Propriedade canônico de PidLidFlagRequest

  
  
**Aplica-se a**: Outlook 
  
Representa o status de uma solicitação de reunião.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidRequest  <br/> |
|Propriedade definida:  <br/> |PSETID_Common  <br/> |
|ID de longo (LID):  <br/> |0x00008530  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Sinalizando  <br/> |
   
## <a name="remarks"></a>Coment�rios

No Microsoft Office Outlook, uma solicitação de reunião é um item de compromisso.
  
Essa propriedade contém texto especificáveis de usuário a ser associado com o sinalizador e deve ser definida se o objeto de mensagem foi sinalizado ou concluído, mas não deve existir para um objeto de reuniões. Os clientes podem optar por não suporte para essa propriedade e sempre escrever "Acompanhamento" (traduzido para o idioma do usuário, se apropriado) como o valor da cadeia de caracteres quando essa propriedade deverá ser definida. Esta propriedade deve ser ignorada condicionalmente com base nos valores das propriedades **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) e **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas a sinalização.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedade canônico para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md)

