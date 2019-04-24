---
title: Tipos de restrições
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0d3bd58b-7100-4117-91ac-27139715c85b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 28159dfb947b4fb0ea54680627588b7c10bee3b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356564"
---
# <a name="types-of-restrictions"></a>Tipos de restrições

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há muitos tipos de restrições, algumas que se concentram em colunas específicas. Todas as implementações de tabelas devem suportar restrições nas colunas no conjunto de colunas atual. No enTanto, para adicionar valor, os implementadores de tabela também podem suportar restrições com base nas propriedades de objeto que não estão atualmente no modo de exibição de tabela.
  
Algumas restrições podem ser combinadas usando uma restrição que executa uma operação lógica **and**, **or**ou **not** . Por exemplo, a maioria das restrições de propriedade deve ser associada a restrições Exists using **e** Restrictions. Há algumas exceções, como quando a propriedade usada na restrição de propriedade é a propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) ou quando é uma coluna obrigatória em uma tabela. Uma restrição de construção de cliente para limitar o modo de exibição deve usar restrições Exists com suas restrições de propriedade porque MAPI não especifica como os provedores de serviços devem avaliar as restrições de propriedade quando uma propriedade não existir. É razoável e recomendado que os provedores de serviços falham na restrição, mas não há nenhum requisito. 
  
Uma restrição é definida usando a estrutura de dados [SRestriction](srestriction.md) que contém uma União de estruturas de restrição mais especializadas e um indicador do tipo de estrutura incluído na União. 
  
Cada uma das estruturas de restrição especializadas na União representa um tipo diferente de restrição. Os tipos de restrições e suas estruturas de dados associadas são:
  
|**Tipo de restrição**|**Estrutura de dados associada**|**Descrição**|
|:-----|:-----|:-----|
|Propriedade Compare  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Compara duas propriedades do mesmo tipo.  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Executa uma operação **e** lógica em duas ou mais restrições.  <br/> |
|**OU** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Executa uma operação lógica **ou** em duas ou mais restrições.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Executa uma operação **não** lógica em duas ou mais restrições.  <br/> |
|Conteúdo  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Localiza dados especificados.  <br/> |
|Propriedade	  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Especifica um determinado valor de propriedade como critérios de correspondência. Pode ser usado, por exemplo, para pesquisar um determinado tipo de anexo.  <br/> |
|Mascara  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Aplica um bitmask a uma propriedade PT_LONG, geralmente para determinar se determinados sinalizadores estão definidos.  <br/> |
|Tamanho  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Testa o tamanho de uma propriedade usando operadores relacionais padrão.  <br/> |
|Existente  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Testa se um objeto tem um valor para uma propriedade.  <br/> |
|Subobjeto  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Usada para pesquisar por subobjetos ou objetos que não podem ser acessados com um identificador de entrada, como destinatários e anexos. Pode ser usado, por exemplo, para procurar mensagens de um destinatário específico.  <br/> |
|Comentário  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Associa um objeto com um conjunto de propriedades nomeadas.  <br/> |
   
Algumas restrições usam expressões regulares e o MAPI oferece suporte a uma forma limitada de notação de expressão regular no estilo que é usado em muitos aplicativos de texto.
  
A restrição de comentário é usada por clientes que salvam restrições no disco para manter as informações específicas do aplicativo com a restrição. Por exemplo, um cliente que salva o nome de uma propriedade nomeada usada em uma restrição de propriedade pode fazê-lo com uma restrição de comentário. Não é possível salvar o nome em uma restrição de propriedade; a estrutura de dados [SPropertyRestriction](spropertyrestriction.md) contém apenas a marca de propriedade. As restrições de comentário são ignoradas por imApitable [:: Restrict](imapitable-restrict.md) no que não têm efeito nas linhas retornadas por IMAPITable [:: QueryRows](imapitable-queryrows.md) após uma chamada **restrita** ter sido feita. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

