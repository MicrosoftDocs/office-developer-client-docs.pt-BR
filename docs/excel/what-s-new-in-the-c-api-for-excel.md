---
title: Novidades na API de C para Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007], novidades
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439685"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Novidades na API de C para Excel

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Em conjunto com o Microsoft Excel 2013, o Microsoft Excel 2013 XLL Software Development Kit (SDK) inclui suporte para os seguintes recursos.
  
- **Novas funções**
    
    O Microsoft Excel 2013 XLL SDK dá suporte à chamada de volta para todas as novas funções de planilha no Excel 2013. For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).
    
- **Funções assíncronas definidas pelo usuário**
    
    O Excel 2013 dá suporte à chamada assíncrona de funções definidas pelo usuário (UDF), o que pode melhorar o desempenho habilitando vários cálculos ao mesmo tempo. Para obter mais informações sobre UDFs assíncronas, consulte Funções de User-Defined [assíncronas.](asynchronous-user-defined-functions.md)
    
- **Conectores de cluster**
    
    Os conectores de cluster permitem que as UDFs executem em clusters de computação de alto desempenho. Para obter mais informações sobre como criar conectores de cluster, consulte [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).
    
    > [!NOTE]
    > Os complementos XLL que você pretende executar em clusters de computação devem chamar apenas funções seguras para cluster. Para obter mais informações sobre as funções que você pode usar, consulte Excel [XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md). 
  
- **Suporte de 64 bits**
    
    Agora você pode compilar e vincular XLLs de 32 bits e 64 bits. Para obter mais informações, consulte [Criando XLLs](creating-xlls.md).
    
## <a name="see-also"></a>Confira também



[Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)
  
[Programação com a API de C no Excel](programming-with-the-c-api-in-excel.md)
  
[Contenção de memória e multithreading no Excel](multithreading-and-memory-contention-in-excel.md)


[Introdução ao Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

