---
title: Função IIf (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Verifica se uma condição é atendida e retorna um valor se VERDADEIRO de outro em caso de falso.
ms.openlocfilehash: 274a923a96b58421f365b03c566a3a1c16b7c48c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439076"
---
# <a name="iif-function-access-custom-web-app"></a>Função IIf (aplicativo Web personalizado do Access)

Verifica se uma condição é atendida e retorna um valor se VERDADEIRO de outro em caso de falso.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

**IIf** (*Condition*, *TrueValue*, *FalseValue*) 
  
A **função IIf** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Condition*  <br/> |A expressão que você deseja avaliar.  <br/> |
| *TrueValue*  <br/> |Valor ou expressão retornado se  *Condição*  for True.  <br/> |
| *FalseValue*  <br/> |Valor ou expressão retornado se  *Condição*  for False.  <br/> |
   
## <a name="example"></a>Exemplo

A expressão a seguir pode ser usada para exibir o nome completo de uma pessoa quando a tabela contém os campos Nome, Nome do Meio e Sobrenome. Se o campo Nome do Meio estiver em branco, apenas os campos de Nome e Sobrenome serão combinados para exibir o nome completo.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


