---
title: Função CONCATENAR (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: Retorna uma cadeia de caracteres com o resultado da combinação de dois ou mais valores de cadeia de caracteres.
ms.openlocfilehash: fc0de43e5e42cc1c39ee89cf76058b8039daf279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765040"
---
# <a name="concat-function-access-custom-web-app"></a>Função CONCATENAR (aplicativo da web personalizado do Access)

Retorna uma cadeia de caracteres com o resultado da combinação de dois ou mais valores de cadeia de caracteres.
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Syntax

**Concat** (*Value1*, *Value2*,... [*ValueN*]) 
  
A função **Concat** contém os seguintes argumentos. 
  
|**Nome do Argumento**|**Description**|
|:-----|:-----|
|Value  <br/> |Um valor de cadeia de caracteres a ser concatenado para outros valores.  <br/> |
   
## <a name="remarks"></a>Remarks

A função **Concat** concatena um número de variável de argumento de cadeia de caracteres em uma única cadeia de caracteres. É necessário haver um mínimo de dois argumentos de cadeia de caracteres, do contrário ocorrerá um erro. 
  
Todos os argumentos são implicitamente convertidos em tipos de dados de cadeia de caracteres e, em seguida, concatenados.
  
## <a name="example"></a>Example

A expressão a seguir pode ser usada para exibir o nome completo de uma pessoa em um dos campos da tabela Nome, Sobrenome e Nome do Meio. Se o campo MiddleInitial estiver vazio, somente os campos FirstName e LastName são combinados para exibir o nome completo.
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


