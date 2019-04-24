---
title: Integração com o Office em aplicativos universais do Windows
manager: soliver
ms.date: 02/06/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60b4fa23-0075-4f6a-8bd0-9e53e99432d5
description: Você pode integrar seu aplicativos de terceiros da plataforma de aplicativos universais do Windows com o Word Mobile, Excel Mobile e PowerPoint Mobile. Os aplicativos universais são integrados com os aplicativos do Office por meio de contratos do seletor de arquivos do Windows, propriedades expando e contratos do Atualizador de Arquivos em Cache.
ms.openlocfilehash: ad04ccc3ceb6e0f1d53e4aebc12cf9724ab8ab66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299758"
---
# <a name="integrate-with-office-from-windows-universal-apps"></a>Integração com o Office em aplicativos universais do Windows

Você pode integrar seu aplicativos de terceiros da plataforma de aplicativos universais do Windows com o Word Mobile, Excel Mobile e PowerPoint Mobile. Os aplicativos universais são integrados com os aplicativos do Office por meio de [contratos do seletor de arquivos do Windows](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx), [propriedades expando](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx) e [contratos do Atualizador de Arquivos em Cache](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).
  
Quando você integra seu aplicativo universal ao Excel, PowerPoint ou Word Mobile, os usuários podem abrir documentos do Office fornecidos pelo seu aplicativo quando navegam no Office ou quando usam o Windows para abrir arquivos no seu aplicativo. Os usuários também podem salvar o arquivo novamente no seu aplicativo universal, que carrega o arquivo de volta ao seu serviço.
  
Os arquivos abertos dessa maneira aparecem na lista Recentes no Office, para que seus usuários possam encontrá-los e reabri-los com facilidade.
  
Essa integração requer que o aplicativo universal:
    
- Implemente os [contratos do seletor de arquivos](https://msdn.microsoft.com/library/windows/apps/hh465174.aspx) do Windows.
    
- Represente um repositório de arquivos (por exemplo, um aplicativo que permite o acesso ao armazenamento em nuvem).
    
## <a name="expando-properties"></a>Propriedades expando

Os aplicativos universais do Windows podem usar propriedades Expando para comunicar informações adicionais associadas a arquivos. Para saber mais sobre como isso funciona no Windows, confira "System.ExpandoProperties" em [StorageItemContentProperties.SavePropertiesAsync](https://msdn.microsoft.com/library/windows/apps/xaml/hh770655.aspx).
  
A tabela a seguir descreve as propriedades que seu aplicativo precisa fornecer ao Office para habilitar cenários de abertura de arquivos. Se essas informações não forem fornecidas, todos os arquivos do seu aplicativo serão abertos como somente leitura. A possibilidade de que os usuários abram arquivos para edição dependerá do tipo de licença do Office que eles possuem e do tipo de documento que estão tentando abrir.
  
Configure essas propriedades no conjunto de propriedades **System.ExpandoProperties**. 
  
|**Property**|**Descrição**|**Tipo**|**Exemplo**|
|:-----|:-----|:-----|:-----|
|**AppDisplayName** <br/> |Nome do provedor a ser exibido para o usuário. Aparece em vários locais no Office, como na lista de documentos recentes.  <br/> |String  <br/> |Contoso  <br/> |
|**MicrosoftOfficeOwnershipType** <br/> |Para licenciamento, indique se o documento/local é Pessoal/Consumidor ou Trabalho/Negócios. Os valores permitidos são (pessoal) 1 e 2 (comercial). Por exemplo, se o arquivo do usuário for armazenado na empresa Contoso, use o valor "2" para comercial.  <br/> |Unit32  <br/> | 1 ou 2  <br/> Por exemplo, se o arquivo do usuário for armazenado na empresa Contoso, o arquivo deverá ser marcado como 2, para comercial.  <br/> |
|**MicrosoftOfficeTermsOfUse** <br/> |Texto jurídico para declarar que as informações fornecidas são corretas de acordo com nossos termos de uso. Esse texto não é exibido para o usuário. Trata-se de um contrato entre você, o provedor do aplicativo, e a Microsoft.  <br/> Confira o exemplo a seguir.  <br/> | String  <br/> | Eu concordo com os termos localizados em [https://go.microsoft.com/fwlink/p/?LinkId=528381](third-party-applications-integrating-with-office-mobile-products.md) <br/> |
   
O exemplo de código a seguir mostra como definir essas propriedades.
  
```cs
public static async Task SetExpandoProperties(StorageFile file,... other params ...) 
  { 
     var expandoProperties = new PropertySet(); 
     expandoProperties.Add("AppDisplayName", "Contoso",);  
     // String value. 
     expandoProperties.Add("MicrosoftOfficeOwnershipType", 1);  
     // Unit32 value - 1 (for personal), 2 (for business).  
     expandoProperties.Add("MicrosoftOfficeTermsOfUse", "I agree to the terms located at https://go.microsoft.com/fwlink/p/?LinkId=528381");   
    // String value. 
          
       var fileProperties = new PropertySet(); 
       fileProperties.Add("System.ExpandoProperties", expandoProperties); 
       await file.Properties.SavePropertiesAsync(fileProperties); 
  } 

```

## <a name="cached-file-updater-contracts"></a>Contratos do Atualizador de Arquivos em Cache

Se o seu aplicativo universal participar dos contratos do Atualizador de Arquivos em Cache, ele será notificado sobre alterações que outro aplicativo universal (como o Office) fizer no arquivo. Para saber mais sobre como isso funciona no Windows, confira [classe CachedFileUpdater](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).
  
O Office usa a opção **AllowOnlyReaders** para abrir os arquivos de leitura-gravação que seu aplicativo universal fornece por meio de contratos do seletor de arquivos. Isso significa que o arquivo não pode ser movido, excluído, renomeado ou gravado por outro aplicativo, como o seu, enquanto ele está aberto no Office. O Office salvará automaticamente o arquivo, mas definirá CachedFileManager.DeferUpdates para impedir a ativação do seu aplicativo até que o Office feche o documento ou até que o Office seja suspenso pelo Windows (quando o usuário alternar para outro aplicativo). Quando o Office fechar o arquivo, seu aplicativo poderá gravar nele. 
  
Seu aplicativo deve lidar com todas as comunicações do seu serviço, incluindo download, atualização e carregamento.
  
As tabelas a seguir listam os parâmetros a serem definidos para lidar com as interações entre seu aplicativo e o Office.
  
|**Parâmetro**|**Descrição**|
|:-----|:-----|
|[ReadActivationMode](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.readactivationmode.aspx) <br/> |Defina **BeforeAccess** para permitir que seu aplicativo atualize o arquivo antes de enviá-lo ao Office.  <br/> |
|[WriteActivationMode](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.writeactivationmode.aspx) <br/> |Defina **ReadOnly** para tornar o arquivo somente leitura. Defina **AfterWrite** para garantir que o aplicativo será acionado por CacheFileUpdater quando o Office concluir o arquivo.<br/><br/>**OBSERVAÇÃO**: se você não definir **AfterWrite**, seu aplicativo não será notificado para carregar as alterações, ou seja, as alterações do usuário serão apenas locais.           |
|[CachedFileOptions.RequireUpdateOnAccess](https://msdn.microsoft.com/library/windows/apps/windows.storage.provider.cachedfileoptions.aspx) <br/> |Defina esta propriedade para garantir que o aplicativo possa atualizar o arquivo quando um usuário acessá-lo na lista Recentes.  <br/> |
   
## <a name="invoking-office-from-your-app"></a>Invocar o Office pelo seu aplicativo

Quando o usuário abre um documento do Office pelo seu aplicativo, o documento pode ser aberto no Word Mobile, Excel Mobile e PowerPoint Mobile. Por exemplo, quando um usuário seleciona um arquivo \*.docx no seu aplicativo, o Word Mobile é iniciado com o arquivo \*.docx aberto. O aplicativo do Office que é aberto se baseia no aplicativo que o usuário associou ao tipo de arquivo.
  
Para abrir um arquivo pelo seu aplicativo no Office, recomendamos que você utilize **LaunchFileAsync()**. Não é recomendável usar **LaunchUriAsync()** para abrir o arquivo porque isso fará com que o aplicativo registrado no esquema URI seja iniciado (o navegador) em vez do Office. Embora **LaunchUriAsync()** com a opção **LauncherOptions.ContentType()** possa invocar o Office, nesse caso o arquivo aberto será marcado como temporário e será somente leitura no Office. 
  
Para saber mais, confira [Classe Launcher](https://msdn.microsoft.com/library/windows/apps/windows.system.launcher.aspx).
  
## <a name="temporary-and-read-only-files"></a>Arquivos temporários e somente leitura

Defina o atributo **FILE_ATTRIBUTE_TEMPORARY** em arquivos temporários e o atributo **FILE_ATTRIBUTE_READONLY** em arquivos somente leitura em seu aplicativo. 
  
Arquivos com os atributos **FILE_ATTRIBUTE_TEMPORARY** ou **FILE_ATTRIBUTE_READONLY** definidos são abertos como somente leitura no Office. O **FILE_ATTRIBUTE_TEMPORARY** também impede que o arquivo apareça na lista Recentes. 
  
Para saber mais sobre atributos de arquivos, confira a [função SetFileAttributes](https://msdn.microsoft.com/library/windows/desktop/aa365535%28v=vs.85%29.aspx).
  
## <a name="other-best-practices"></a>Outras práticas recomendadas

Para otimizar a consistência do arquivo, por exemplo, quando ocorrerem erros ou conflitos em edições, aplique as seguintes práticas recomendadas:
  
- Impeça que os conflitos sejam salvos.
    
  - Pause os carregamentos quando ocorrerem conflitos de servidor para evitar bifurcação (permita bifurcação somente quando o Office não tiver mais um arquivo de gravação aberto). Normalmente, se um arquivo do seu aplicativo for aberto do Office, o aplicativo será ativado apenas quando o Office for fechado ou suspenso pelo Windows.
    
  - Se você precisar de interface do usuário para resolver conflitos, implemente as notificações do sistema. A interface do usuário completa não está disponível quando o Office é suspenso.
    
- Lide com erros.
    
  - Quando um bloqueio for liberado, notifique os usuários sobre o conflito e forneça um caminho para resolvê-lo no seu aplicativo.
    
## <a name="see-also"></a>Confira também

- [Integração com o Office](integrate-with-office.md)   
- [Integração com o Office em clientes de sincronização do Win32](integrate-with-office-from-win32-sync-clients.md)
    

