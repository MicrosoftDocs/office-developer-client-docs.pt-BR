---
title: Função Concat (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Retorna uma cadeia de caracteres com o resultado da combinação de dois ou mais valores de cadeia de caracteres.
ms.openlocfilehash: b8f52c292e64939f9464bc666ecc4bc341580f94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282289"
---
# <a name="concat-function-access-custom-web-app"></a>Função Concat (aplicativo Web personalizado do Access)

Retorna uma cadeia de caracteres com o resultado da combinação de dois ou mais valores de cadeia de caracteres.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

**Concat** (*Valor1*, *Valor2*, …[*ValorN*]) 
  
A função **Concat** contém os seguintes argumentos. 
  
|**Nome do Argumento**|**Descrição**|
|:-----|:-----|
|Valor  <br/> |Um valor de cadeia de caracteres a ser concatenado para outros valores.  <br/> |
   
## <a name="remarks"></a>Comentários

A função **Concat** concatena um número de variável de argumento de cadeia de caracteres em uma única cadeia de caracteres. É necessário haver um mínimo de dois argumentos de cadeia de caracteres, do contrário ocorrerá um erro. 
  
Todos os argumentos são implicitamente convertidos em tipos de dados de cadeia de caracteres e, em seguida, concatenados.
  
## <a name="example"></a>Exemplo

A expressão a seguir pode ser usada para exibir o nome completo de uma pessoa quando a tabela contém os campos Nome, Nome do Meio e Sobrenome. Se o campo Nome do Meio estiver em branco, apenas os campos de Nome e Sobrenome serão combinados para exibir o nome completo.
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


