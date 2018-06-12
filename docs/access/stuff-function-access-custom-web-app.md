---
title: Função coisas (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Insere uma cadeia de caracteres de texto em outra cadeia de caracteres de texto. Ela exclui um tamanho especificado de caracteres na primeira cadeia de caracteres na posição inicial e, em seguida, insere a segunda cadeia a primeira cadeia de caracteres na posição inicial.
ms.openlocfilehash: 5540bb5936803370835a0c3d80b420edc13d0de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765232"
---
# <a name="stuff-function-access-custom-web-app"></a>Função coisas (aplicativo da web personalizado do Access)

Insere uma cadeia de caracteres de texto em outra cadeia de caracteres de texto. Ela exclui um tamanho especificado de caracteres na primeira cadeia de caracteres na posição inicial e, em seguida, insere a segunda cadeia a primeira cadeia de caracteres na posição inicial.
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Syntax

 **Coisas** (*IntoTextExpression*, *Iniciar*, *comprimento*, *ThisTextExpression*) 
  
A função **coisas** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |Uma expressão de texto que especifica o texto no qual o texto especificado pelo *ThisTextExpression* será inserido.  <br/> |
| *Start*  <br/> |Um valor integer que especifica o local para iniciar a inserção e exclusão. Se o início ou o comprimento for negativo, uma cadeia de caracteres nula será retornada. Se start for maior que o primeiro *IntoTextExpression* , uma cadeia de caracteres nula será retornada.  <br/> |
| *Length*  <br/> |Um inteiro que especifica o número de caracteres a ser excluído. Se length for maior que o primeiro *IntoTextExpression* , exclusão ocorre até o último caractere no último *IntoTextExpression* .  <br/> |
| *ThisTextExpression*  <br/> |Um texto chapéu de expressão Especifica o texto para inserir em *IntoTextExpression* . Esta expressão substituirá os caracteres de comprimento de início de *IntoTextExpression* em *Iniciar* .  <br/> |
   
## <a name="remarks"></a>Coment�rios

Se os argumentos *Iniciar* ou *comprimento* são negativos, ou se a posição inicial for maior que o comprimento da cadeia de caracteres primeiro, uma cadeia de caracteres nula será retornada. Se a posição inicial for 0, é retornado um valor nulo. Se o comprimento para excluir for maior que a primeira cadeia de caracteres, ele é excluído para o primeiro caractere na primeira cadeia de caracteres. 
  

