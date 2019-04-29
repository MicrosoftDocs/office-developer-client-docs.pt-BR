---
title: Função Count (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Retorna o número de registros em uma consulta ou tabela.
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419139"
---
# <a name="count-function-access-custom-web-app"></a>Função Count (aplicativo Web personalizado do Access)

Retorna o número de registros em uma consulta ou tabela.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

**Contagem** (*Expressão*) 
  
A função **Count** contém o argumento a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Expressão*  <br/> |Uma expressão de cadeia de caracteres identificando o campo que contém os dados que você deseja contar ou uma expressão que executa um cálculo usando os dados no campo. Os operandos na *expressão* podem incluir o nome de um campo de tabela ou função (que pode ser intrínseco ou definido pelo usuário, mas não outras funções de agregação SQL). É possível contar qualquer tipo de dados, inclusive texto.  <br/> |
   
## <a name="remarks"></a>Comentários

Você pode usar Count para contar o número de registros em uma consulta de base. Por exemplo, você poderia usar Count para contar o número de pedidos enviados para um determinado país ou região.
  
**Contagem** (\*) retorna o número de itens em um grupo. Isso inclui valores nulos e duplicatas. 
  

