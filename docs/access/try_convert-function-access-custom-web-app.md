---
title: Try_Convert (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Converte um valor em um tipo de dados especificado ou retorna Null se a conversão não for válida.
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410893"
---
# <a name="try_convert-function-access-custom-web-app"></a>Try_Convert (aplicativo Web personalizado do Access)

Converte um valor em um tipo de dados especificado ou retorna Null se a conversão não for válida.
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="syntax"></a>Sintaxe

 **Try_Convert** (*DataType*, *Expression*) 
  
A **Try_Convert** função contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *DataType*  <br/> |O tipo de dados no qual converter  *expressão*  .  <br/> |
| *Expressão*.  <br/> |O valor a ser convertido.  <br/> |
   
## <a name="remarks"></a>Comentários

 **Try_Convert** o valor passado para ele e tenta convertê-lo para o *DataType especificado.* Se a conversão for **bem-sucedida, Try_Convert** retornará o valor como  *DataType especificado;*  se ocorrer um erro, será retornado null. No entanto, se você solicitar uma conversão explicitamente não permitida, **Try_Convert** falhará com um erro. 
  

