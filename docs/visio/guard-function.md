---
title: Função GUARD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
localization_priority: Normal
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: Protege a expressão contra exclusão e alteração por ações executadas na janela de desenho, por exemplo, movendo, tamanho, agrupando ou desagrupando formas.
ms.openlocfilehash: 0bdfa023d53e739a970cab65b1dbd67bc1a44461
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408149"
---
# <a name="guard-function"></a>Função GUARD

Protege a  *expressão*  contra exclusão e alteração por ações executadas na janela de desenho, por exemplo, movendo, tamanho, agrupando ou desagrupando formas. 
  
## <a name="syntax"></a>Sintaxe

GUARD(** *expressão* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor.  <br/> |
   
## <a name="remarks"></a>Comentários

As células normalmente afetadas pela função GUARD são Width, Height, PinX e PinY. 
  
Proteger uma fórmula em qualquer célula evita que o valor da célula seja alterado por ações executadas na janela de desenho. No entanto, uma ação na janela de desenho pode afetar diversas células e cada uma dessas células deve estar protegida caso você deseje evitar alterações inesperadas na aparência da forma. 
  
## <a name="example"></a>Exemplo

GUARD(TEXTWIDTH(TheText) + 0,5 pol.) 
  
Esta expressão na célula Width de uma seção Shape Transform de uma forma impede que a expressão (TEXTWIDTH(TheText) + 0,5 pol.) seja substituída por outro valor quando a largura da forma for alterada na janela de desenho. TheText é uma célula disparada quando a composição do texto da forma associada é alterada. 
  

