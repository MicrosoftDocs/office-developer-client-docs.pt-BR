---
title: Ação de Macro ExecutarMacrodeDados (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: Você pode usar a ação ExecutarMacrodeDados para executar uma macro de dados independentes.
ms.openlocfilehash: 55a0ff4c731dc517c5d71aa20d8e46c3b4ff4611
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765218"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a>Ação de Macro ExecutarMacrodeDados (aplicativo da web personalizado do Access)

Você pode usar a ação **ExecutarMacrodeDados** para executar uma macro de dados independentes. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A ação **ExecutarMacrodeDados** tem os seguintes argumentos. 
  
|**Argumento da ação**|**Descrição**|
|:-----|:-----|
| _Macro Name_ <br/> |O nome da macro de dados a ser executada.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando você selecionar a macro de dados que deseja executar no designer de macros, o Access determinará se a macro de dados exige parâmetros. Se a macro de dados requer parâmetros, caixas de texto aparecem onde você pode digitar nos argumentos.
  
Quando você executa uma macro que contém a ação **ExecutarMacrodeDados** e ela alcançar a ação **ExecutarMacrodeDados**, o Access executará a macro de dados chamada. Após a conclusão da macro de dados chamada, o Access retornará à macro original e executará a próxima ação. 
  

