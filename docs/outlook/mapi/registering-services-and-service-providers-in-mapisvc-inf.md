---
title: Registrar provedores de serviços e serviços no MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Modificado pela última vez: 18 de julho de 2013'
ms.openlocfilehash: c74257b84636952b26c5a624f4f7f76f66be9149
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566919"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Registrar provedores de serviços e serviços no MapiSvc.inf

 
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A instalação de um novo provedor em um sistema requer atualizando o arquivo Mapisvc para apontar para o novo provedor. Propriedades padrão definida durante a configuração, que incluem o seguinte, informam MAPI onde encontrar a biblioteca de vínculo dinâmico do provedor (. dll):
  
- O **PR_SERVICE_DLL_NAME** é especificado na seção **[Serviço de mensagem]** . 
    
- O **PR_PROVIDER_DLL_NAME** é especificado na seção **[Serviço provedor]** . 
    
> [!NOTE]
> A expectativa é que você defina o nome do. dll do seu provedor (sem o sufixo "32"). MAPI então carrega o seu provedor procurando por ela no caminho. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Colocar um caminho em MAPISVC

A maioria dos aplicativos são instalados em arquivos de programas que requerem uma atualização para a variável path para permitir que os provedores MAPI trabalhar. Com algumas restrições Microsoft Outlook 2010 e o Outlook 2013 podem acomodar caminhos completos para provedores MAPI.
  
Ao registrar seu provedor no Mapisvc, você poderia colocar o caminho completo para o provedor nas propriedades do MAPI **PR_SERVICE_DLL_NAME** e **PR_PROVIDER_DLL_NAME**.
  
Em ambas as propriedades o caminho completo deve estar sem o sufixo "32", porque MAPI continua a acrescente que o nome do arquivo antes procurando o arquivo. Isso significa que se registrar o caminho "c:\mypath\myprovider.dll", MAPI tentará carregar "c:\mypath\myprovider32.dll".
  
Porque do Outlook MAPI não foi originalmente criado para acomodar os caminhos completos, ele realiza a inserção do sufixo "32" observando para o primeiro período na cadeia de caracteres, o que significa que os caminhos que contêm outros períodos não podem funcionar, portanto, você não pode usar caminhos como "c:\my.path\myprovider.dll" ou "c:\mypath\my.provider.dll".
  
Em alguns casos, em um provedor de armazenamento você irá gerar identificadores de entrada usando a função **WrapStoreEntryID** , que tem como um parâmetro, o nome do seu provedor. 
  
> [!IMPORTANT]
> Se você estiver usando caminhos completos em MAPISVC, você deve usar o mesmo caminho em todas as chamadas para **WrapStoreEntryID**. 
  
Além disso, o caminho que você usar pode ser convertido em Unicode usando a página de código fornecida pela função [GetACP](http://msdn.microsoft.com/en-us/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) . 
  
> [!CAUTION]
> Fica falha se você escolher um caminho que contém caracteres que não podem sobreviver tal uma ida e volta por meio das funções [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) e [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) . 
  
Para obter uma demonstração dessa funcionalidade, a [amostra de PST quebrado automaticamente](http://ol2010mapisamples.codeplex.com/) no CodePlex foi revisado - a funcionalidade pertinente está em **MergeWithMapiSvc** e **GenerateProviderPath**.
  

