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
ms.openlocfilehash: 7e3459c639cac449cdc03361949c9618827515b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770633"
---
# <a name="types-of-restrictions"></a>Tipos de restrições

  
  
**Aplica-se a**: Outlook 
  
Há muitos tipos de restrições, alguns que se concentrem em colunas específicas. Todas as implementações de tabela esperadas para dar suporte a restrições nas colunas no conjunto atual de coluna. No entanto, para adicionar um valor, implementadores de tabela também podem oferecer suporte restrições com base nas propriedades do objeto que não estão atualmente no modo de exibição de tabela.
  
Algumas restrições podem ser combinadas usando uma restrição que está executando uma operação de lógica **e**, **ou**ou **não** . Por exemplo, a propriedade maioria das restrições devem estar associadas com existir restrições usando **e** restrições. Há algumas exceções, como quando a propriedade usada na restrição de propriedade é a propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) ou quando ela é uma coluna necessária em uma tabela. Um cliente de criação de restrições para limitar o seu modo de exibição deve usar existir restrições com restrições de sua propriedade porque MAPI não especifica como provedores de serviços devem avaliar restrições de propriedade quando uma propriedade não existe. É razoável e recomendado que a restrição de falhar de provedores de serviço, mas não existem requisitos. 
  
Uma restrição é definida usando a estrutura de dados [SRestriction](srestriction.md) que contém uma união de estruturas de restrição mais especializadas e um indicador do tipo de estrutura incluído na União. 
  
Cada as estruturas de restrição especializados na União representa um tipo diferente de restrição. Os tipos de restrições e suas estruturas de dados associados são:
  
|**Tipo de restrição**|**Estrutura de dados associados**|**Descrição**|
|:-----|:-----|:-----|
|Comparar a propriedade  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Compara duas propriedades do mesmo tipo.  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Executa uma operação **AND** lógica em dois ou mais restrições.  <br/> |
|**OU** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Executa uma operação **OR** lógica em dois ou mais restrições.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Executa uma operação **não é** lógica em dois ou mais restrições.  <br/> |
|Content  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Localiza os dados especificados.  <br/> |
|Propriedade  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Especifica um valor de propriedade específica como critérios de correspondência. Pode ser usado, por exemplo, para pesquisar por um determinado tipo de anexo.  <br/> |
|Bitmask  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Aplica uma máscara de bits para uma propriedade PT_LONG, geralmente para determinar se a determinado sinalizadores estão definidos.  <br/> |
|Size  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Testa o tamanho de uma propriedade usando operadores relacionais padrão.  <br/> |
|Existe  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Testa se um objeto tem um valor para uma propriedade.  <br/> |
|Subobjeto  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Usado para pesquisar o subobjetos ou objetos que não podem ser acessados com um identificador de entrada, como destinatários e anexos. Pode ser usado, por exemplo, para procurar mensagens para um destinatário específico.  <br/> |
|Comment  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Associa um objeto com um conjunto de propriedades nomeadas.  <br/> |
   
Algumas restrições usam expressões regulares e MAPI oferece uma forma limitada de expressão regular a notação no estilo que é usada muitos aplicativos de texto.
  
A restrição de comentário é usada pelos clientes que salvar restrições em disco para manter informações específicas de aplicativo com a restrição. Por exemplo, um cliente a salvando o nome de uma propriedade nomeada usado em uma restrição de propriedade poderá fazer isso com uma restrição de comentário. Salvar o nome não é possível em uma restrição de propriedade; a estrutura de dados [SPropertyRestriction](spropertyrestriction.md) contém apenas a marca de propriedade. Restrições de comentário serão ignoradas pelo [IMAPITable:: Restrict](imapitable-restrict.md) em que eles não têm efeito sobre as linhas retornadas pela [IMAPITable:: QueryRows](imapitable-queryrows.md) após ter sido feita uma chamada **Restrict** . 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

