---
title: Registrando provedores de serviços e serviços no MapiSvc.inf
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
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Registrando provedores de serviços e serviços no MapiSvc.inf

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A instalação de um novo provedor em um sistema requer a atualização do arquivo MapiSvc.inf para apontar para o novo provedor. Propriedades padrão definidas durante a configuração, que incluem o seguinte, informam ao MAPI onde encontrar a biblioteca de vínculo dinâmico do provedor (.dll):
  
- A **PR_SERVICE_DLL_NAME** é especificada na **seção [Serviço de** Mensagens]. 
    
- O **PR_PROVIDER_DLL_NAME** especificado na seção **[Provedor de** Serviços]. 
    
> [!NOTE]
> A expectativa é que você de definir o nome da .dll do provedor (sem o sufixo "32"). MAPI then loads your provider by looking for it on the path. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Colocando um caminho em MapiSvc.inf

A maioria dos aplicativos é instalada em Arquivos de Programas, exigindo uma atualização na variável de caminho para permitir que provedores MAPI funcionem. Com algumas restrições, o Microsoft Outlook 2010 e o Outlook 2013 podem acomodar caminhos completos para provedores mapi.
  
Ao registrar seu provedor em MapiSvc.inf, você pode colocar o caminho completo para o provedor nas propriedades MAPI **PR_SERVICE_DLL_NAME** e **PR_PROVIDER_DLL_NAME**.
  
Em qualquer uma das propriedades, o caminho completo deve estar sem o sufixo "32", pois o MAPI continua anexando-o ao nome do arquivo antes de procurar o arquivo. Isso significa que, se você registrar o caminho "c:\mypath\myprovider.dll", o MAPI tentará carregar "c:\mypath\myprovider32.dll".
  
Como o MAPI do Outlook não foi originalmente projetado para acomodar caminhos completos, ele realiza essa inserção do sufixo "32" procurando pelo primeiro período na cadeia de caracteres, o que significa que caminhos que contêm outros períodos não podem funcionar, portanto, você não pode usar caminhos como "c:\my.path\myprovider.dll" ou "c:\mypath\my.provider.dll".
  
Às vezes, em um provedor de repositório, você gera identificadores de entrada usando a **função WrapStoreEntryID,** que usa como parâmetro o nome do seu provedor. 
  
> [!IMPORTANT]
> Se você estiver usando caminhos completos em MapiSvc.inf, deverá usar o mesmo caminho em qualquer chamada para **WrapStoreEntryID**. 
  
Além disso, o caminho usado pode ser convertido de e para Unicode usando a página de código fornecida pela [função GetACP.](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) 
  
> [!CAUTION]
> Haverá falha se você escolher um caminho que contenha caracteres que não podem sobreviver a tal ida e volta por meio das funções [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) e [WideCharToMultiByte.](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) 
  
Para uma demonstração dessa funcionalidade, o exemplo [PST](https://github.com/stephenegriffin/Outlook2010CodeSamples) empacotado no GitHub foi revisado - a funcionalidade pertinente está em **MergeWithMapiSvc** e **GenerateProviderPath**.
  

