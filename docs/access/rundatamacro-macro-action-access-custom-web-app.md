---
title: Ação de macro ExecutarMacrodeDados (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Você pode usar a ação RunDataMacro para executar uma macro de dados autônoma.
ms.openlocfilehash: 68c0e5a3837039bdab1165e686adb3bdf2a5b6f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439342"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a>Ação de macro ExecutarMacrodeDados (aplicativo Web personalizado do Access)

Você pode usar a **ação RunDataMacro** para executar uma macro de dados autônoma. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A ação **ExecutarMacrodeDados** tem os seguintes argumentos. 
  
|**Argumento da ação**|**Descrição**|
|:-----|:-----|
| _Macro Name_ <br/> |O nome da macro de dados a ser executada.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando você selecionar a macro de dados que deseja executar no designer de macros, o Access determinará se a macro de dados exige parâmetros. Se a macro de dados exigir parâmetros, as caixas de texto aparecerão onde você poderá digitar os argumentos.
  
Quando você executa uma macro que contém a ação **ExecutarMacrodeDados** e ela alcançar a ação **ExecutarMacrodeDados**, o Access executará a macro de dados chamada. Após a conclusão da macro de dados chamada, o Access retornará à macro original e executará a próxima ação. 
  

