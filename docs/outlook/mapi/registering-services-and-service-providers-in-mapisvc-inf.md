---
title: Registrar serviços e provedores de serviços no MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Última modificação: 18 de julho de 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328368"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Registrar serviços e provedores de serviços no MapiSvc. inf

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A instalação de um novo provedor em um sistema requer a atualização do arquivo MapiSvc. inf para apontar para o novo provedor. Propriedades padrão definidas durante a configuração, que incluem o seguinte, informe MAPI onde encontrar a biblioteca de vínculo dinâmico do provedor (. dll):
  
- O **PR_SERVICE_DLL_NAME** é especificado na seção **[Message Service]** . 
    
- O **PR_PROVIDER_DLL_NAME** é especificado na seção **[provedor de serviços]** . 
    
> [!NOTE]
> A expectativa é que você defina o nome do. dll do provedor (sem o sufixo "32"). Em seguida, o MAPI carrega seu provedor procurando-o no caminho. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Colocar um caminho no MapiSvc. inf

A maioria dos aplicativos é instalada em arquivos de programa, exigindo uma atualização para a variável path para permitir que os provedores MAPI funcionem. Com algumas restrições, o Microsoft Outlook 2010 e o Outlook 2013 podem acomodar caminhos completos para provedores MAPI.
  
Ao registrar seu provedor no MapiSvc. inf, você poderia colocar o caminho completo para o provedor nas propriedades MAPI **PR_SERVICE_DLL_NAME** e **PR_PROVIDER_DLL_NAME**.
  
Em qualquer uma das propriedades, o caminho completo deve estar sem o sufixo "32", porque o MAPI continua a anexá-lo ao nome do arquivo antes de procurar seu arquivo. Isso significa que, se você registrar o caminho "c:\mypath\myprovider.dll", o MAPI tentará carregar "c:\mypath\myprovider32.dll".
  
Como o MAPI do Outlook não foi originalmente projetado para acomodar caminhos completos, ele realiza essa inserção do sufixo "32" procurando o primeiro período na cadeia de caracteres, o que significa que os caminhos que contêm outros períodos não podem funcionar, portanto, não é possível usar caminhos como "c:\My.path\myprovider.dll" ou "c:\mypath\my.Provider.dll".
  
Às vezes, em um provedor de repositório, você irá gerar identificadores de entrada usando a função **WrapStoreEntryID** , que usa como um parâmetro o nome do provedor. 
  
> [!IMPORTANT]
> Se você estiver usando caminhos completos no MapiSvc. inf, deverá usar o mesmo caminho em todas as chamadas para o **WrapStoreEntryID**. 
  
Além disso, o caminho que você usa pode ser convertido em e de Unicode usando a página de código fornecida pela função [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) . 
  
> [!CAUTION]
> Você terá uma falha se escolher um caminho que contenha caracteres que não podem sobreviver a um percurso de ida e volta às funções [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) e [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) . 
  
Para uma demonstração dessa funcionalidade, o [exemplo de PST encapsulado](https://github.com/stephenegriffin/Outlook2010CodeSamples) no GitHub foi revisado-a funcionalidade pertinente está no **MergeWithMapiSvc** e no **GenerateProviderPath**.
  

