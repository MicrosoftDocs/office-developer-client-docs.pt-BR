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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357782"
---
# <a name="pidlidflagstring-canonical-property"></a>Propriedade canônica PidLidFlagString

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um índice que identifica um dos conjuntos de cadeias de caracteres de texto predefinidos associados ao sinalizador.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidFlagStringEnum  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085C0  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Tarefa  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade for definida, os clientes devem usar o valor de cadeia de caracteres correspondente nas tabelas abaixo (por exemplo, para substituir uma cadeia de caracteres que é traduzida no idioma do usuário atual) e deve ignorar o valor definido em **dispidFlagRequest** ([ PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) e **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)). 
  
Os padrões sugeridos para os objetos de contato do usuário são os seguintes:
  
|**Valor**|**Cadeia de caracteres em inglês**|
|:-----|:-----|
|0x00000000 ou não presente  <br/> | Siga as orientações relacionadas à exibição do **dispidFlagRequest**.  <br/> |
|0x0000006E  <br/> |"Acompanhamento"  <br/> |
|0x0000006F  <br/> |Receptor  <br/> |
|0x00000070  <br/> |"Organizar reunião"  <br/> |
|0x00000071  <br/> |"Enviar email"  <br/> |
|0x00000072  <br/> |"Enviar carta"  <br/> |
   
Os padrões sugeridos para o usuário para todos os outros objetos de mensagem são os seguintes:
  
|**Valor**|**Cadeia de caracteres em inglês**|
|:-----|:-----|
|0x00000000 ou não presente  <br/> | Siga as orientações relacionadas à exibição do **dispidFlagRequest**.  <br/> |
|0x00000001  <br/> |Receptor  <br/> |
|0x00000002  <br/> |"Não enCaminhar"  <br/> |
|0x00000003  <br/> |"Acompanhamento"  <br/> |
|0x00000004  <br/> |"Para suas informações"  <br/> |
|0x00000005  <br/> |Direta  <br/> |
|0x00000006  <br/> |"Nenhuma resposta necessária"  <br/> |
|0x00000007  <br/> |Saiba  <br/> |
|0x00000008  <br/> |Resposta  <br/> |
|0x00000009  <br/> |"Responder a todos"  <br/> |
|Interrupção  <br/> |Exame  <br/> |
   
Todas as cadeias de caracteres especificadas acima podem ser traduzidas para o idioma do usuário, se apropriado.
  
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

