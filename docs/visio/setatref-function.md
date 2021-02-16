---
title: Função SETATREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
localization_priority: Normal
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: Redireciona valores atualizados resultantes de ações na interface do usuário (UI) ou automação para outra célula.
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416801"
---
# <a name="setatref-function"></a>Função SETATREF

Redireciona valores atualizados resultantes de ações na interface do usuário (UI) ou automação para outra célula. 
  
## <a name="syntax"></a>Sintaxe

SETATREF(** *reference* ** [, ** *set_expression* ** [, ** *ignore_eval* ** ]]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _reference_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma referência à célula para a qual as atualizações são redirecionadas.  <br/> |
| _set_expression_ <br/> |Opcional  <br/> |**String** <br/> |Uma expressão que é atribuída para _referência._  <br/> |
| _ignore_eval_ <br/> |Opcional  <br/> |**Boolean** <br/> |Se for VERDADEIRO, a função SETATREF será avaliada como (0) zero; se FALSE (o padrão) a função SETATREF é avaliada como o valor de  _referência_.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando uma ação do usuário na janela de desenho ou um método automation faz com que o Microsoft Visio atualize uma célula contendo uma fórmula SETATREF, o valor é redirecionado para a célula referenciada pela fórmula SETATREF (referência). A fórmula da célula que contém a função SETATREF permanece intacta.
  
Se  _set_expression_ for omitido, o valor definido na interface do usuário ou usando Automação será atribuído à célula referenciada; caso contrário, o conteúdo  _set_expression_ será atribuído à célula referenciada. Isso permite que o novo valor seja modificado ou transformado antes de ser atribuído à célula referenciada. 
  
A função SETATREF possui duas funções relacionadas: 
  
- A função SETATREFEXPR, que você pode usar para representar o novo valor em  _set_expression_. Por exemplo, uma  _set_expression_ de SETATREFEXPR()-2 in. poderia ser usado para subtrair 2 polegadas do resultado SETATREFEXPR. 
    
- A função SETATREFEVAL, que você pode usar  para indicar que alguma parte da set_expression deve ser avaliada e substituída por seu resultado. 
    
A função SETATREF foi projetada para uso em células que podem ser alteradas por ações do usuário na janela de desenho. Há suporte para as seguintes células:
  
- seção ShapeTransform — células Width, Height, Angle, PinX e PinY
    
- seção Text Transform — células TxtWidth, TxtHeight, TxtAngle, TxtPinX e TxtPinY
    
- seção 1-D Endpoints  — células BeginX, BeginY, EndX e EndY
    
- seção Controls — células Controls.X e Controls.Y
    
- Seção Shape Data
    
Como SETATREF altera o local onde os valores das células mudam, ela afeta a emissão de eventos. Se uma célula contém SETATREF, os eventos **FormulaChanged** e **CellChanged** são emitidos para a célula referenciada por SETATREF, e não para a célula contendo SETATREF. Se uma célula que contém SETATREF também contiver SETATREFEXPR, o evento **FormulaChanged** também será a disparar para a célula que contém SETATREF porque um parâmetro de função é alterado. 
  
Outros pontos importantes a serem observados sobre a função SETATREF são:
  
- As funções SETATREF podem encadear até 10 referências a outras funções SETATREF. 
    
- As células podem conter outras expressões além da função SETATREF, inclusive várias ocorrências de SETATREF em uma única célula.
    
- Se as formas estiverem coladas, o Visio segue a cadeia de referência SETATREF dentro da mesma planilha e coloca fórmulas de cola na célula referenciada. 
    
- A automação reconhece a função SETATREF e segue a cadeia de células referenciadas. 
    
- Assim como GUARD, SETATREF não protege as células contra alterações feitas usando a função SETF na ShapeSheet.
    
## <a name="example1"></a>Exemplo1

Digamos que uma forma tem uma propriedade personalizada chamada Width, e a célula Width da seção Shape Transform contém a seguinte fórmula:
  
=SETATREF(Prop.Width)
  
Se um usuário alterar a largura da forma na interface do usuário, o novo valor será atribuído à célula Prop.Width, não à célula Width da seção ShapeTransform; a fórmula na célula Width permanece inalterada. Você também pode definir a largura da forma usando os dados da forma.
  
## <a name="example2"></a>Exemplo2

As soluções do Visio geralmente têm formas com uma relação hierárquica, o que faz com que as formas filhas movam quando uma forma pai é movida. A seguir, um exemplo de como você poderia gerenciar essa relação usando a função SETATREF na ShapeSheet. 
  
As fórmulas a seguir estão na seção Shape Transform da forma filha. Além disso, definimos células do usuário chamadas User.DeltaX e User.DeltaY, que rastreiam a dimensão de deslocamento de ParentShape. Isso permite que a forma filha mova quando a forma pai é movida e também preserva a relação hierárquica se a forma filha é movida.
  
PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX
  
PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY
  
Quando a forma filha é movida usando a interface do usuário, os novos valores PinX e PinY são definidos como o parâmetro na função SETATREFEXPR. A função SETATREF avalia a fórmula entre SETATREFEVAL e substitui PinX e PinY por seus resultados e, em seguida, a fórmula resultante é atribuída às células do usuário referenciadas na função SETATREF User.DeltaX e User.DeltaY. Finalmente, os valores retornados por SETATREF (User.DeltaX ou User.DeltaY) são adicionados ao local do pino de ParentShape para calcular o local do pino da forma filha.
  

