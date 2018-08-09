---
title: Função CALLTHIS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
localization_priority: Normal
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Chama um procedimento em um Microsoft Visual Basic para o project Applications (VBA).
ms.openlocfilehash: 04065384453e55b745daa89273fb4c23b32fb90c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771432"
---
# <a name="callthis-function"></a>Função CALLTHIS

Chama um procedimento em um Microsoft Visual Basic para o project Applications (VBA).
  
## <a name="syntax"></a>Sintaxe

CALLTHIS ("* * *procedimento* * *", ["* * *project* * *"], [* * *arg1* * *, * * *arg2* * *,...]) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _procedimento_ <br/> |Obrigatório  <br/> |**String** <br/> | O nome do procedimento a ser chamado.  <br/> |
| _Project_ <br/> |Opcional  <br/> |**String** <br/> |O projeto que contém o procedimento.  <br/> |
| _arg_ <br/> |Opcional  <br/> |**Número, Cadeia de Caracteres, Data ou Moeda** <br/> |Passados como parâmetros para o procedimento.  <br/> |
   
## <a name="remarks"></a>Comentários

No projeto VBA, o *procedimento* é definida da seguinte maneira: 
  
procedimento (*vsoshape as* Visio. Shape [arg1 As type, arg2 As type...]) 
  
onde *vsoshape as* é uma referência ao objeto **Shape** que contém a fórmula CALLTHIS sendo avaliada e _arg1_, *arg2* ... são os argumentos especificados na fórmula. 
  
Observe que *vsoshape as* é muito parecido com o argumento "this" passado a um procedimento de membro C++; daí o nome "CALLTHIS." Na verdade, uma célula que contém uma fórmula que inclui CALLTHIS pode ser lido como "Chamar esse procedimento e passe uma referência para a minha forma". 
  
Se o _projeto_ for especificado, o Microsoft Visio verifica todos os documentos abertos para o um contendo _project_ e chamadas de _procedimento_ no projeto. Se o _projeto_ for omitido ou nulo (""), Visio pressupõe que o _procedimento_ está no projeto VBA do documento que contém a fórmula CALLTHIS que está sendo avaliada. 
  
Números em _arg1_, _arg2 …_ são passados em unidades externas. Por exemplo, se você passar o valor da célula Height de uma forma que é 3 centímetros de altura, 3 é passado. Para passar unidades diferentes com um número, use a função FORMATEX ou force explicitamente as unidades adicionando um par de unidade numérica nulo, por exemplo, 0 pés + altura. 
  
A segunda vírgula na função CALLTHIS é opcional. Ela corresponde ao número de parâmetros adicionais adicionados ao procedimento. Se você não usa nenhum parâmetro adicional, exceto `(vsoShape as Visio.Shape)` , não adicione a segunda vírgula; Use CALLTHIS("",). Se você adicionar dois parâmetros adicionais, por exemplo, use CALLTHIS. 
  
A função CALLTHIS sempre avalia como 0, e a chamada para o _procedimento_ ocorre durante o tempo ocioso após a conclusão do processo de recálculo.  _Procedimento_ pode retornar um valor, mas ignorado pelo Visio.  _Procedimento_ retorna um valor que o Visio pode reconhecer, definindo o resultado da outra célula ou uma fórmula no documento, mas não para a célula que chamou o _procedimento_, a menos que você deseja substituir a fórmula CALLTHIS.
  
A função CALLTHIS difere da função RUNADDON no sentido de que o projeto de um documento não precisa fazer referência a um outro projeto para chamar esse projeto. 
  
> [!NOTE]
>  O código VBA, que é invocado quando a instância do Visio avalia uma função CALLTHIS em uma fórmula, não deve fechar o documento que contém a célula que está usando a função, uma vez que ocorrerá um erro de aplicativo e o Visio será fechado. 
  
Se você precisar fechar o documento que contém a célula que está utilizando a função CALLTHIS, utilize uma das técnicas a seguir: 
  
- Feche o documento a partir de um código que não seja VBA.
    
- Feche o documento a partir de um projeto diferente do que está sendo fechado.
    
- Envie mensagens de janela para fechar as janelas em vez de fechar o documento.
    
Para obter mais informações sobre a execução de códigos no Visio, consulte [Sobre configurações de segurança e execução de códigos no Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) nesta Referência da ShapeSheet. 
  
## <a name="example-1"></a>Exemplo 1

CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))
  
Chamará o procedimento p, localizado em um módulo, e passará o valor de altura em centímetros, como 7,62 cm.
  
## <a name="example-2"></a>Exemplo 2

CALLTHIS("q",,0 cm+Height,Width)
  
Chamará o procedimento q, localizado em um módulo, e passará a altura da célula em centímetros e a largura em unidades internas.
  
## <a name="example-3"></a>Exemplo 3

Use o procedimento a seguir no módulo de classe *ThisDocument* . 
  
Utilize uma das sintaxes a seguir na célula EventDblClick de uma forma com os procedimentos descritos anteriormente.
  
CALLTHIS("ThisDocument.A",)
  
CALLTHIS("ThisDocument.B",,"Click")
  
CALLTHIS("Este documento.C",,"Clique", " OK.")
  

