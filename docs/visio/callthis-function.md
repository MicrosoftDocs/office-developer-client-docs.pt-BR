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
description: Chama um procedimento em um projeto do Microsoft Visual Basic for Applications (VBA).
ms.openlocfilehash: 7e0f0bafa39d6c1eb1fd39535506981c937ce8a1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337237"
---
# <a name="callthis-function"></a>Função CALLTHIS

Chama um procedimento em um projeto do Microsoft Visual Basic for Applications (VBA).
  
## <a name="syntax"></a>Sintaxe

CALLTHIS ("* * *procedimento* * *", ["* * *project* * *"], [* * *arg1* * *, * * *arg2* * *,...]) 
  
### <a name="parameters"></a>Parâmetros

|**Nome**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _procedimento_ <br/> |Obrigatório  <br/> |**String** <br/> | O nome do procedimento a ser chamado.  <br/> |
| _projeto_ <br/> |Opcional  <br/> |**String** <br/> |O projeto que contém o procedimento.  <br/> |
| _ARG_ <br/> |Opcional  <br/> |**Número, Cadeia de Caracteres, Data ou Moeda** <br/> |Passados como parâmetros para o procedimento.  <br/> |
   
## <a name="remarks"></a>Comentários

No projeto VBA, o *procedimento* é definido da seguinte maneira: 
  
procedimento (*vsoShape* como Visio. Shape [arg1 as Type, arg2 as Type...]) 
  
onde *vsoShape* é uma referência ao objeto **Shape** que contém a fórmula CALLTHIS que está sendo avaliada e _arg1_, *arg2* ... os argumentos são especificados na fórmula. 
  
Observe que *vsoShape* é muito parecido com o argumento "This" passado para um procedimento de membro C++; Portanto, o nome "CALLTHIS". Na verdade, uma célula que contém uma fórmula que inclui CALLTHIS pode ser lida como "chamar este procedimento e passar uma referência para minha forma". 
  
Se o _projeto_ for especificado, o Microsoft Visio examinará todos os documentos abertos para o que você contém o _projeto_ e as chamadas de _procedimento_ nesse projeto. Se _Project_ for omitido ou nulo (""), o Visio pressupõe que o _procedimento_ está no projeto VBA do documento que contém a fórmula CALLTHIS que está sendo avaliada. 
  
Os números em _arg1_, _arg2..._ são passados em unidades externas. Por exemplo, se o valor da célula Height for passado de uma forma de 3 centímetros de altura, 3 será o valor passado. Para passar unidades diferentes com um número, utilize a função FORMATEX ou force explicitamente as unidades adicionando um par de unidade de número nulo, por exemplo, 0 pés + Altura. 
  
A segunda vírgula na função CALLTHIS é opcional. Ela corresponde ao número de parâmetros adicionais adicionados ao procedimento. Se você não usar nenhum parâmetro adicional, exceto `(vsoShape as Visio.Shape)` , não adicione a segunda vírgula; Use CALLTHIS ("",). Se você adicionar dois parâmetros opcionais, por exemplo, utilize CALLTHIS("",,,). 
  
A função CALLTHIS sempre é avaliada como 0 e a chamada para o _procedimento_ ocorre durante o tempo ocioso após a conclusão do processo de recálculo.  O _procedure_ poderá retornar um valor, mas será ignorado pelo Visio.  _Procedure_ retorna um valor que o Visio pode reconhecer Configurando a fórmula ou o resultado de outra célula no documento, mas não a célula que chamou o _procedimento_, a menos que você queira substituir a fórmula CALLTHIS.
  
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
  
CALLTHIS ("ThisDocument. A",)
  
CALLTHIS ("ThisDocument. B", "clique")
  
CALLTHIS("Este documento.C",,"Clique", " OK.")
  

