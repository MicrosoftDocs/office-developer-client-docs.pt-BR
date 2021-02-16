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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416283"
---
# <a name="types-of-restrictions"></a>Tipos de restrições

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Há muitos tipos de restrições, alguns que se concentram em colunas específicas. Espera-se que todas as implementações de tabela suportem restrições nas colunas no conjunto de colunas atual. No entanto, para adicionar valor, implementadores de tabela também podem dar suporte a restrições com base em propriedades de objeto que não estão atualmente no exibição de tabela.
  
Algumas restrições podem ser combinadas usando uma restrição que executa uma operação **lógica AND**, **OR** ou **NOT.** Por exemplo, a maioria das restrições de propriedade deve ser unidas com restrições existentes usando **restrições AND.** Há algumas exceções, como quando a propriedade usada na restrição de propriedade é a propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) ou quando é uma coluna necessária em uma tabela. As restrições de construção de um cliente para limitar sua exibição devem usar restrições existentes com suas restrições de propriedade porque o MAPI não especifica como os provedores de serviços devem avaliar as restrições de propriedade quando uma propriedade não existe. É razoável e recomendado que os provedores de serviços falhem na restrição, mas não há requisitos. 
  
Uma restrição é definida usando a estrutura de dados [SRestriction,](srestriction.md) que contém uma união de estruturas de restrição mais especializadas e um indicador do tipo de estrutura incluída na união. 
  
Cada uma das estruturas de restrição especializadas na união representa um tipo diferente de restrição. Os tipos de restrições e suas estruturas de dados associadas são:
  
|**Tipo de restrição**|**Estrutura de dados associada**|**Descrição**|
|:-----|:-----|:-----|
|Propriedade Compare  <br/> |[SComparePropsRestriction](scomparepropsrestriction.md) <br/> |Compara duas propriedades do mesmo tipo.  <br/> |
|**AND** <br/> |[SAndRestriction](sandrestriction.md) <br/> |Executa uma operação **AND** lógica em duas ou mais restrições.  <br/> |
|**OU** <br/> |[SOrRestriction](sorrestriction.md) <br/> |Executa uma operação **OR lógica** em duas ou mais restrições.  <br/> |
|**NOT** <br/> |[SNotRestriction](snotrestriction.md) <br/> |Executa uma operação **LÓGICA NOT** em duas ou mais restrições.  <br/> |
|Conteúdo  <br/> |[SContentRestriction](scontentrestriction.md) <br/> |Localiza dados especificados.  <br/> |
|Propriedade  <br/> |[SPropertyRestriction](spropertyrestriction.md) <br/> |Especifica um valor de propriedade específico como critério para correspondência. Pode ser usado, por exemplo, para pesquisar um tipo específico de anexo.  <br/> |
|Bitmask  <br/> |[SBitMaskRestriction](sbitmaskrestriction.md) <br/> |Aplica uma máscara de bits a uma PT_LONG, normalmente para determinar se sinalizadores específicos estão definidos.  <br/> |
|Size  <br/> |[SSizeRestriction](ssizerestriction.md) <br/> |Testa o tamanho de uma propriedade usando operadores relacionais padrão.  <br/> |
|Exist  <br/> |[SExistRestriction](sexistrestriction.md) <br/> |Testa se um objeto tem um valor para uma propriedade.  <br/> |
|Subobjeto  <br/> |[SSubRestriction](ssubrestriction.md) <br/> |Usado para pesquisar subobjetos ou objetos que não podem ser acessados com um identificador de entrada, como destinatários e anexos. Pode ser usado, por exemplo, para procurar mensagens para um destinatário específico.  <br/> |
|Comentário  <br/> |[SCommentRestriction](scommentrestriction.md) <br/> |Associa um objeto a um conjunto de propriedades nomeadas.  <br/> |
   
Algumas restrições usam expressões regulares, e MAPI oferece suporte a uma forma limitada de notação de expressão regular no estilo que é usado em muitos aplicativos de texto.
  
A restrição de comentário é usada por clientes que salvam restrições no disco para manter informações específicas do aplicativo com a restrição. Por exemplo, um cliente que salva o nome de uma propriedade nomeada usada em uma restrição de propriedade pode fazê-lo com uma restrição de comentário. Não é possível salvar o nome em uma restrição de propriedade; a [estrutura de dados SPropertyRestriction](spropertyrestriction.md) contém apenas a marca de propriedade. As restrições de comentário são ignoradas por [IMAPITable::Restrict](imapitable-restrict.md) no sentido de que elas não têm efeito nas linhas retornadas por [IMAPITable::QueryRows](imapitable-queryrows.md) após uma chamada **Restrict** ter sido feita. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

