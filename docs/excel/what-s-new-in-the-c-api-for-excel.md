---
title: Quais são as novidades do C API para Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- a api c [excel 2007], o que há de novo
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19765440"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Quais são as novidades do C API para Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Em conjunto com o Microsoft Excel 2013, o Microsoft Excel 2013 XLL Software Development Kit (SDK) inclui o suporte para os recursos a seguintes.
  
- **Novas funções**
    
    O Microsoft Excel 2013 XLL SDK suporta chamar de volta todas as novas funções de planilha no Excel 2013. Para obter mais informações sobre como chamar funções do Excel 2013, consulte [ligações para o Excel a partir da DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md).
    
- **Funções assíncronas definidas pelo usuário**
    
    Excel 2013 suporta chamando funções definidas pelo usuário (UDF) de forma assíncrona, que podem melhorar o desempenho, permitindo que vários cálculos executar ao mesmo tempo. Para obter mais informações sobre UDFs assíncronos, consulte [Asynchronous User-Defined funções](asynchronous-user-defined-functions.md).
    
- **Conectores de cluster**
    
    Conectores de cluster habilitar UDFs executar em clusters de computação de alto desempenho. Para obter mais informações sobre a criação de conectores de cluster, consulte [Desenvolvendo conectores de Cluster do Excel](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > Suplementos XLL que você pretende executar em clusters de computadores devem chamar apenas as funções de cluster-safe. Para obter mais informações sobre as funções, você pode usar, consulte [Referência de função de API do Excel XLL SDK](excel-xll-sdk-api-function-reference.md) e [Funções de segurança do Cluster](cluster-safe-functions.md). 
  
- **Suporte de 64 bits**
    
    Agora você pode compilar e vincular XLLs de 32 bits e 64 bits. Para obter mais informações, consulte [Criando XLLs](creating-xlls.md).
    
## <a name="see-also"></a>Confira também



[Developing Excel XLLs](developing-excel-xlls.md)
  
[Programando com a API C no Excel](programming-with-the-c-api-in-excel.md)
  
[Multithreading e contenção de memória no Excel](multithreading-and-memory-contention-in-excel.md)


[Getting Started with the Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

