---
title: Adesão a função (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Retorna a primeira expressão não for nula de uma lista de argumentos.
ms.openlocfilehash: cfe6f59c22a89b2a6d211e5f05c2dbf275d8da11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765070"
---
# <a name="coalesce-function-access-custom-web-app"></a>Adesão a função (aplicativo da web personalizado do Access)

Retorna a primeira expressão não for nula de uma lista de argumentos.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

**União** (*Valor*, [*valor*],..., [*valor*]) 
  
A função de **adesão** contém os seguintes argumentos 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Valor*  <br/> |Uma expressão.  <br/> |
   
## <a name="remarks"></a>Coment�rios

Se todos os argumentos forem NULL, **adesão** retornará NULL. 
  
## <a name="example"></a>Example

A expressão a seguir é usada como a regra de validação para uma tabela. A expressão garante que as entradas são feitas nos campos nome, último nome, Email, telefone celular, trabalho, Home telefone, e companhia telefônica antes que um registro seja confirmado. Se qualquer um dos campos listados forem deixadas em branco, a função de **adesão** retornará Null, o que viola a regra de validação. 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


