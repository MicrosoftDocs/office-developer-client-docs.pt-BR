---
title: Propriedade canônica PidLidFlagString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395578"
---
# <a name="pidlidflagstring-canonical-property"></a>Propriedade canônica PidLidFlagString

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um índice que identifica um conjunto de cadeias de caracteres de texto predefinido associado com o sinalizador.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidFlagStringEnum  <br/> |
|Propriedade definida:  <br/> |PSETID_Common  <br/> |
|ID de longo (LID):  <br/> |0x000085C0  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade estiver definida, os clientes devem usar o valor de cadeia de caracteres correspondente nas tabelas a seguir (por exemplo, para substituir uma cadeia de caracteres que é traduzida no idioma do usuário atual) e devem ignorar o valor definido no **dispidFlagRequest** ([ PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) e **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)). 
  
Padrões sugeridos para o usuário para objetos de contato são:
  
|**Valor**|**Cadeia de caracteres de inglês**|
|:-----|:-----|
|0x00000000 ou não está presente  <br/> | Siga as orientações relacionadas à exibindo **dispidFlagRequest**.  <br/> |
|0x0000006E  <br/> |"Acompanhamento"  <br/> |
|0x0000006F  <br/> |"Chamada"  <br/> |
|0x00000070  <br/> |"Organizar reuniões"  <br/> |
|0x00000071  <br/> |"Enviar Email"  <br/> |
|0x00000072  <br/> |"Enviar a letra"  <br/> |
   
Padrões sugeridos para o usuário para todos os outros objetos de mensagem são os seguintes:
  
|**Valor**|**Cadeia de caracteres de inglês**|
|:-----|:-----|
|0x00000000 ou não está presente  <br/> | Siga as orientações relacionadas à exibindo **dispidFlagRequest**.  <br/> |
|0x00000001  <br/> |"Chamada"  <br/> |
|0x00000002  <br/> |"Não encaminhar"  <br/> |
|0x00000003  <br/> |"Acompanhamento"  <br/> |
|0x00000004  <br/> |"Para sua informação"  <br/> |
|0x00000005  <br/> |"Encaminhar"  <br/> |
|0x00000006  <br/> |"Não é preciso responder"  <br/> |
|0x00000007  <br/> |"Ler"  <br/> |
|0x00000008  <br/> |"Reply"  <br/> |
|0x00000009  <br/> |"Responder a todos os"  <br/> |
|0x0000000A  <br/> |"Revisão"  <br/> |
   
Todas as cadeias de caracteres especificadas acima podem ser traduzidas para o idioma do usuário, se apropriado.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas a sinalização.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

