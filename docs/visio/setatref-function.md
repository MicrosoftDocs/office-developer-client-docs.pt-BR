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
description: Redirecionamentos atualizado valores resultantes das ações na interface do usuário (UI) ou automação para outra célula.
ms.openlocfilehash: 69a9cb93ae3fbd807ef4f306be386f5389a6cfeb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772863"
---
# <a name="setatref-function"></a>Função SETATREF

Redirecionamentos atualizado valores resultantes das ações na interface do usuário (UI) ou automação para outra célula. 
  
## <a name="syntax"></a>Sintaxe

SETATREF (* * *referência* * * [, * * *set_expression* * * [, * * *ignorar_aval* * *]]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _referência_ <br/> |Obrigatório  <br/> |**String** <br/> |Uma referência à célula para a qual as atualizações são redirecionadas.  <br/> |
| _Set_Expression_ <br/> |Opcional  <br/> |**String** <br/> |Uma expressão que é atribuída à _referência_.  <br/> |
| _ignorar_aval_ <br/> |Opcional  <br/> |**Boolean** <br/> |Se verdadeiro, a função SETATREF avalia como (0) zero; Se for falso (o padrão) a função SETATREF avalia como o valor da _referência_.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando uma ação do usuário na janela de desenho, ou um método de automação, faz o Microsoft Visio atualize uma célula contendo uma fórmula SETATREF, o valor é redirecionado para a célula referenciada pela fórmula SETATREF ( _referência_). A fórmula da célula que contém a função SETATREF permanece intacta.
  
Se _set_expression_ for omitido, o valor definido na interface de usuário ou por meio da automação é atribuído à célula referenciada; Caso contrário, o conteúdo de _set_expression_ é atribuído à célula referenciada. Isso permite que o novo valor a ser modificado ou transformado antes de ser atribuído à célula referenciada. 
  
A função SETATREF possui duas funções relacionadas: 
  
- A função SETATREFEXPR, que você pode usar para representar o novo valor dentro de _set_expression_. Por exemplo, um _set_expression_ de SETATREFEXPR ()-2 pol. pode ser usada para subtrair 2 polegadas do resultado de SETATREFEXPR. 
    
- A função SETATREFEVAL, que você pode usar para indicar que uma parte de _set_expression_ deve ser avaliada e substituída por seu resultado. 
    
A função SETATREF é projetada para uso em células que podem ser alterados por ações do usuário na janela de desenho. As células a seguir são suportadas:
  
- seção ShapeTransform — células Width, Height, Angle, PinX e PinY
    
- seção Text Transform — células TxtWidth, TxtHeight, TxtAngle, TxtPinX e TxtPinY
    
- seção 1-D Endpoints  — células BeginX, BeginY, EndX e EndY
    
- seção Controls — células Controls.X e Controls.Y
    
- Seção Shape Data
    
Como SETATREF altera o local onde os valores das células mudam, ela afeta o acionamento de eventos. Se uma célula contém SETATREF, os eventos **FormulaChanged** e **CellChanged** é acionado para a célula referenciada por SETATREF, e não a célula contendo SETATREF. Se uma célula contendo SETATREF também contiver SETATREFEXPR, o evento **FormulaChanged** também é acionado para a célula contendo SETATREF porque um parâmetro de função é alterado. 
  
Outros pontos importantes a serem observados sobre a função SETATREF são:
  
- As funções SETATREF podem encadear até 10 referências a outras funções SETATREF. 
    
- As células podem conter outras expressões além da função SETATREF, inclusive várias ocorrências de SETATREF em uma única célula.
    
- Se as formas estiverem coladas, o Visio segue a cadeia de referência SETATREF dentro da mesma planilha e coloca fórmulas de cola na célula referenciada. 
    
- A automação reconhece a função SETATREF e segue a cadeia de células referenciadas. 
    
- Assim como GUARD, SETATREF não protege as células contra alterações feitas usando a função SETF na ShapeSheet.
    
## <a name="example1"></a>Example1

Digamos que uma forma tem uma propriedade personalizada chamada Width, e a célula Width da seção Shape Transform contém a seguinte fórmula:
  
=SETATREF(prop.Width)
  
Se um usuário alterar a largura da forma na interface de usuário, o novo valor é atribuído à célula Prop. Width, não à célula Width da seção ShapeTransform; a fórmula na célula Width permanecerá inalterada. Você também pode definir a largura da forma usando os dados da forma.
  
## <a name="example2"></a>Example2

As soluções do Visio geralmente têm formas com uma relação hierárquica, o que faz com que as formas filhas movam quando uma forma pai é movida. A seguir, um exemplo de como você poderia gerenciar essa relação usando a função SETATREF na ShapeSheet. 
  
As fórmulas a seguir estão na seção Shape Transform da forma filha. Além disso, definimos células do usuário chamadas User.DeltaX e User.DeltaY, que rastreiam a dimensão de deslocamento de ParentShape. Isso permite que a forma filha mova quando a forma pai é movida e também preserva a relação hierárquica se a forma filha é movida.
  
PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX
  
PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY
  
Quando a forma filha é movida usando a interface do usuário, os novos valores PinX e PinY são definidos como o parâmetro na função SETATREFEXPR. A função SETATREF avalia a fórmula contida em SETATREFEVAL e substitui PinX e PinY por seus resultados e, em seguida, a fórmula resultante é atribuída às células do usuário referenciadas no SETATREF DeltaX and DeltaY. Por fim, os valores retornados por SETATREF (DeltaX ou DeltaY) são adicionados ao local do pino de ParentShape para calcular o local do pino da forma filho.
  

