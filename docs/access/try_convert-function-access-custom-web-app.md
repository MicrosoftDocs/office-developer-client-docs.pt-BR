---
title: Função Try_Convert (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Converte um valor em um tipo de dados especificada ou retorna Null se a conversão não é válida.
ms.openlocfilehash: ce942c1f444da7bfcbff76077a5a9d75dd611336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765264"
---
# <a name="tryconvert-function-access-custom-web-app"></a>Função Try_Convert (aplicativo da web personalizado do Access)

Converte um valor em um tipo de dados especificada ou retorna Null se a conversão não é válida.
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Syntax

 **Try_Convert** (*DataType*, *expressão*) 
  
A função **Try_Convert** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Tipo de dados*  <br/> |O tipo de dados no qual converter a *expressão* .  <br/> |
| *Expression*  <br/> |O valor a ser convertido.  <br/> |
   
## <a name="remarks"></a>Coment�rios

 **Try_Convert** leva o valor passado para ele e tenta convertê-lo para o *tipo de dados* de especificado. Se a conversão for bem sucedido, o **Try_Convert** retornará o valor como o *tipo de dados* especificado; Se ocorrer um erro, null será retornado. No entanto se você solicitar uma conversão que explicitamente não é permitida, **Try_Convert** falha com um erro. 
  

