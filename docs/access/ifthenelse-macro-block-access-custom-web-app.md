---
title: Se... Então... Bloco de Macro Else (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Você pode usar a se bloco de macro para executar condicionalmente um grupo de ações, dependendo do valor de uma expressão.
ms.openlocfilehash: 8ac78ff0eaf22c1d821e306654ebfa8fac4ed34a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765080"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a>Se... Então... Bloco de Macro Else (aplicativo da web personalizado do Access)

Você pode usar o bloco de macro **Se** para executar condicionalmente um grupo de ações, dependendo do valor de uma expressão. 
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Syntax

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a>Configuração

Para **Se** e ** Senão Se **, os seguintes argumentos são requeridos. 
  
|**Argumento da ação**|**Descrição**|
|:-----|:-----|
|**Expressão** <br/> |A condição que você deseja testar. Ela deve ser uma expressão que é avaliada como True ou False.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando você seleciona o bloco de macro **Se**, uma caixa de texto é exibida para que você digite uma expressão que representa a condição a ser testada. Além disso, uma caixa de combinação é exibida para que você insira uma ação de macro, abaixo da qual o texto "Encerrar Se" é exibido automaticamente. Se e Encerrar Se delimitam uma área na qual é possível digitar um grupo ou um bloco de ações. O bloco será executado somente se a expressão inserida tiver o valor True. 
  
Para avaliar outra expressão quando a primeira expressão tiver o valor False, clique em **Adicionar Senão Se** para inserir um bloco **Senão Se** adicional. A expressão inserida deve avaliar como True ou False. Nesse caso, o bloco será executado somente se a expressão tiver o valor True e a primeira expressão tiver o valor False. 
  
Você pode adicionar a quantidade necessária de **Senão Se** a um bloco Se. 
  
Clique em **Adicionar Senão** para inserir um bloco **Senão** adicional. Nesse caso, as ações inseridas abaixo de **Senão** formam o bloco **Senão**, que será executado somente se as ações acima não forem executadas. É possível adicionar um único bloco **Senão** a um bloco **Se**. 
  
No exemplo de código a seguir, as ações de macro no primeiro bloco serão executadas se o valor de [Status] for maior que 0. Se o valor de [Status] não for maior que 0, a expressão após **Senão Se** será avaliada. As ações de macro no bloco **Senão Se** serão executadas se o valor de [Status] for igual a 0. Finalmente, se nem o primeiro bloco, nem o segundo forem executados, as ações no bloco **Senão** serão executadas. 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

Você pode aninhar blocos **Se**. Considere o aninhamento do bloco **Se** em um bloco **Se** se você deseja avaliar uma segunda expressão, quando a primeira expressão tiver o valor True. No exemplo de código a seguir, o bloco **Se** interno somente será executado quando o valor de [Status] for maior que 0  *e*  maior que 100. 
  

