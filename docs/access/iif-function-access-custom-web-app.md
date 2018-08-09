---
title: Função IIf (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: Verifica se uma condição for atendida e retorna um valor se for TRUE, de um outro se for FALSE.
ms.openlocfilehash: 26240735341a316a3aed08a12c42e8b6e7af805f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765048"
---
# <a name="iif-function-access-custom-web-app"></a>Função IIf (aplicativo da web personalizado do Access)

Verifica se uma condição for atendida e retorna um valor se for TRUE, de um outro se for FALSE.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

**IIf** (*Condição*, *TrueValue*, *FalseValue*) 
  
A função **IIf** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Condição*  <br/> |A expressão que você deseja avaliar.  <br/> |
| *TrueValue*  <br/> |Expressão ou valor retornado se a *condição* for verdadeira.  <br/> |
| *FalseValue*  <br/> |Expressão ou valor retornado se a *condição* for False.  <br/> |
   
## <a name="example"></a>Exemplo

A expressão a seguir pode ser usada para exibir o nome completo de uma pessoa quando a tabela contém os campos Nome, Nome do Meio e Sobrenome. Se o campo Nome do Meio estiver em branco, apenas os campos de Nome e Sobrenome serão combinados para exibir o nome completo.
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


