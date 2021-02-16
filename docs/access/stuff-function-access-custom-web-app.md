---
title: Função Stuff (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Insere uma cadeia de caracteres de texto em outra cadeia de caracteres de texto. Ele exclui um comprimento especificado de caracteres na primeira cadeia de caracteres na posição inicial e insere a segunda cadeia de caracteres na primeira cadeia de caracteres na posição inicial.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427672"
---
# <a name="stuff-function-access-custom-web-app"></a>Função Stuff (aplicativo Web personalizado do Access)

Insere uma cadeia de caracteres de texto em outra cadeia de caracteres de texto. Ele exclui um comprimento especificado de caracteres na primeira cadeia de caracteres na posição inicial e insere a segunda cadeia de caracteres na primeira cadeia de caracteres na posição inicial.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 **Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*) 
  
A **função Stuff** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |Uma expressão de texto que especifica o texto no qual o texto especificado por  *ThisTextExpression*  será inserido.  <br/> |
| *Start*  <br/> |Um valor inteiro que especifica o local para iniciar a exclusão e a inserção. Se início ou comprimento for negativo, uma cadeia de caracteres nula será retornada. Se o início for maior que o primeiro  *IntoTextExpression*  , uma cadeia de caracteres nula será retornada.  <br/> |
| *Length*  <br/> |Um inteiro que especifica o número de caracteres a excluir. Se o comprimento for maior que o primeiro  *IntoTextExpression*  , a exclusão ocorrerá até o último caractere no último  *IntoTextExpression*  .  <br/> |
| *ThisTextExpression*  <br/> |Um gorro de expressão de texto especifica o texto a ser inserido  *em IntoTextExpression*  . Esta expressão substituirá os caracteres de comprimento  *de IntoTextExpression*  começando em  *Start*  .  <br/> |
   
## <a name="remarks"></a>Comentários

Se os  *argumentos Start*  ou  *Length*  são negativos ou se a posição inicial for maior do que o comprimento da primeira cadeia de caracteres, uma cadeia de caracteres nula será retornada. Se a posição inicial for 0, um valor nulo será retornado. Se o comprimento a ser excluído for maior que a primeira cadeia de caracteres, ele será excluído para o primeiro caractere na primeira cadeia de caracteres. 
  

