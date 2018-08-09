---
title: Excel XLL SDK API Function Reference
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- referência de função de API [excel 2007], funções [Excel 2007], referência [Excel 2007], Excel 2007 XLL Software Development Kit, referência
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765366"
---
# <a name="excel-xll-sdk-api-function-reference"></a>Excel XLL SDK API Function Reference

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O Microsoft Excel 2013 XLL SDK contém os arquivos de origem para uma biblioteca de Framework projetado para acelerar a elaboração XLLs e dois projetos de amostra, exemplo e genérico. 
  
Esta seção fornece uma referência de função para o seguinte:
  
- Retornos de chamada que chamar XLL do Excel.
    
- XLL retornos de chamada que procura o Microsoft Excel.
    
- Funções principais dos projetos de amostra e framework.
    
## <a name="sample-projects"></a>Projetos de amostra

O SDK XLL do Excel 2013 fornece os arquivos de origem e os arquivos de projeto do Microsoft Visual Studio para os projetos de amostra a seguir:
  
- O projeto **Framework** (`SAMPLES\FRAMEWRK\`) contém um projeto que pode ser criado em uma biblioteca de FRAMEWRK.lib, que podem ser vinculados, em seguida, em outros projetos XLL. A biblioteca contém muitas funções e ferramentas que tornam escrever XLLs mais fácil. Esta biblioteca é usada em ambos os outros projetos em conjunto com o arquivo de cabeçalho FRAMEWRK.h.
    
- O projeto de **exemplo** (`SAMPLES\EXAMPLE\`) contém um projeto que pode ser criado para um XLL, EXAMPLE.xll. XLL contém muitos exemplos de implementações de exemplo as funções de interface de Suplemento XLL como **xlAutoOpen**e o uso da biblioteca do Framework.
    
- O projeto **genérico** (`SAMPLES\GENERIC\`) contém um projeto que pode ser criado para um XLL, GENERIC.xll. XLL demonstra as várias funções de exemplo e comandos e é um bom ponto de partida para escrever seus próprios XLLs.
    
## <a name="in-this-section"></a>Nesta seção

- [Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)
  
- [C API Callback Functions Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)
  
- [Funções XLM essenciais e úteis para a API de C](essential-and-useful-c-api-xlm-functions.md)
  
- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [Funções na biblioteca de estrutura](functions-in-the-framework-library.md)
  
- [Funções na DLL genérica](functions-in-the-generic-dll.md)
  
- [Funções de conector de cluster do Excel](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a>Confira também

- [Programar com a API de C no Excel](programming-with-the-c-api-in-excel.md)
  
- [Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

