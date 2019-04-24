---
title: Implementar verbos de formulário padrão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317441"
---
# <a name="implementing-standard-form-verbs"></a>Implementar verbos de formulário padrão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI define um conjunto de verbos padrão ou ações executadas quando um usuário faz uma seleção de menu ou clica em um botão, que todos os visualizadores de formulários devem oferecer suporte. Cada verbo tem uma constante associada a ela para identificação, definida no EXCHFORM. Arquivo de cabeçalho H. A tabela a seguir lista os verbos de formulário padrão e suas constantes associadas:
  
|**Verb**|**Valor**|
|:-----|:-----|
|Abrir  <br/> |EXCHIVERB_OPEN  <br/> |
|Responder  <br/> |EXCHIVERB_REPLYTOSENDER  <br/> |
|Responder a Todos  <br/> |EXCHIVERB_REPLYTOALL  <br/> |
|Encaminhar  <br/> |EXCHIVERB_FORWARD  <br/> |
|Print  <br/> |EXCHIVERB_PRINT  <br/> |
|Salvar como  <br/> |EXCHIVERB_SAVEAS  <br/> |
|Responder para Pasta  <br/> |EXCHIVERB_REPLYTOFOLDER  <br/> |
   
Quando um usuário escolhe um verbo, passe sua constante em uma chamada para o método [IMAPIForm::D overb](imapiform-doverb.md) para executar a ação correspondente. 
  
Além de acessar verbos por meio de seu visualizador de formulários, os usuários podem, às vezes, acessar verbos diretamente no formulário. Por exemplo, alguns objetos Form permitem que o usuário invoque o verbo **Print** clicando com o botão direito do mouse no formulário e escolhendo **Imprimir** de um menu contextual. 
  

