---
title: Integração com o Office a partir de aplicativos universais do Windows
manager: soliver
ms.date: 02/06/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 60b4fa23-0075-4f6a-8bd0-9e53e99432d5
description: É possível integrar seus aplicativos de terceiros plataforma Windows app universal com Excel Mobile, Mobile do PowerPoint e Word Mobile. Aplicativos universais integram-se com aplicativos do Office por meio de contratos de selecionador de arquivo do Windows, propriedades expandido e contratos de cache atualizador de arquivo.
ms.openlocfilehash: 2c170fd55c9c6f10d348610ffbc75ffa86447529
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765721"
---
# <a name="integrate-with-office-from-windows-universal-apps"></a>Integração com o Office a partir de aplicativos universais do Windows

É possível integrar seus aplicativos de terceiros plataforma Windows app universal com Excel Mobile, Mobile do PowerPoint e Word Mobile. Aplicativos universais integram com o Office apps via Windows [contratos de selecionador de arquivo](https://msdn.microsoft.com/en-us/library/windows/apps/hh465174.aspx), [Propriedades expandido](https://msdn.microsoft.com/en-us/library/windows/apps/xaml/hh770655.aspx)e [contratos de cache atualizador de arquivo](https://msdn.microsoft.com/en-us/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).
  
Ao integrar seu aplicativo universal com Excel, PowerPoint ou Word Mobile, os usuários podem abrir documentos do Office que seu aplicativo fornece, ou quando eles pesquisam de dentro do Office ou quando usar o Windows para abrir arquivos a partir do seu aplicativo. Os usuários também podem salvar o arquivo de volta para seu aplicativo universal, que carrega o arquivo de volta para seu serviço.
  
Arquivos abertos dessa maneira aparecem na lista recente no escritório, para que seus usuários possam facilmente encontrar e reabri-los.
  
Essa integração requer que seu aplicativo universal:
    
- Implementa os [contratos de selecionador de arquivo](https://msdn.microsoft.com/en-us/library/windows/apps/hh465174.aspx)do Windows.
    
- Representa um repositório de arquivos (por exemplo, um aplicativo que permite acesso ao armazenamento em nuvem).
    
## <a name="expando-properties"></a>Propriedades expandido

Aplicativos universais do Windows podem usar propriedades expandido para se comunicar informações adicionais que é associadas a arquivos. Para obter informações sobre como isso funciona no Windows, consulte "System.ExpandoProperties" em [StorageItemContentProperties.SavePropertiesAsync](https://msdn.microsoft.com/en-us/library/windows/apps/xaml/hh770655.aspx).
  
A tabela a seguir descreve as propriedades de seu aplicativo para fornecer ao escritório para habilitar cenários de arquivos abertos. Se essas informações não for fornecidas, todos os arquivos do seu aplicativo são abertos como somente leitura. Se os usuários podem abrir arquivos para edição depende do tipo de licença do Office têm e o tipo de documento que está tentando abrir.
  
Defina essas propriedades no conjunto de propriedades **System.ExpandoProperties** . 
  
|**Property**|**Descrição**|**Type**|**Exemplo**|
|:-----|:-----|:-----|:-----|
|**AppDisplayName** <br/> |Nome do provedor para exibir ao usuário. Aparece em vários locais no Office, como a lista de documentos recentes.  <br/> |Cadeia de caracteres  <br/> |Contoso  <br/> |
|**MicrosoftOfficeOwnershipType** <br/> |Para licenciamento, indique se o local do documento/é trabalho/comercial ou pessoal/consumidor. Os valores permitidos são 1 (pessoais) e 2 (comercial). Por exemplo, se o arquivo do seu usuário é armazenado em negócios da Contoso, use o valor "2" para a empresa.  <br/> |Unit32  <br/> | 1 ou 2  <br/> Por exemplo, se o arquivo do seu usuário é armazenado em negócios da Contoso, esse arquivo deve marcado 2 para negócios.  <br/> |
|**MicrosoftOfficeTermsOfUse** <br/> |Texto legal para declarar que as informações fornecidas são precisas por nossos termos de uso. Esse texto não é exibido ao usuário. É um contrato entre você, o provedor de aplicativo e da Microsoft.  <br/> Veja o seguinte para ver um exemplo.  <br/> | Cadeia de caracteres  <br/> | Eu concordar com os termos localizados em[https://go.microsoft.com/fwlink/p/?LinkId=528381](third-party-applications-integrating-with-office-mobile-products.md) <br/> |
   
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

## <a name="cached-file-updater-contracts"></a>Contratos de atualizador do arquivo armazenado em cache

Se seu aplicativo universal participa de contratos de cache atualizador de arquivo, ele será notificado se altera torna de outro aplicativo universal (por exemplo, o Office) para o arquivo. Para obter informações sobre como isso funciona no Windows, consulte [classe de CachedFileUpdater](https://msdn.microsoft.com/en-us/library/windows/apps/windows.storage.provider.cachedfileupdater.aspx).
  
Office usa a opção **AllowOnlyReaders** para abrir os arquivos de leitura-gravação que seu aplicativo universal fornece via os contratos de selecionador de arquivo. Isto significa que o arquivo não pode ser movido, excluídos, renomeados ou gravadas por outro aplicativo, incluindo o seu próprio, enquanto ela está aberta no Office. Office serão salvamento automático o arquivo, mas conjuntos CachedFileManager.DeferUpdates para evitar ativando seu aplicativo até Office fecha o documento ou Office é suspenso pelo Windows (quando o usuário alterna para outro aplicativo). Quando o Office fecha o arquivo, seu aplicativo pode gravar nele. 
  
Seu aplicativo deve lidar com toda a comunicação com o seu serviço, incluindo carregamento, refresh e download.
  
As tabelas a seguir lista os parâmetros para definir como lidar com as interações entre o aplicativo e o Office.
  
|**Parâmetro**|**Descrição**|
|:-----|:-----|
|[ReadActivationMode](https://msdn.microsoft.com/en-us/library/windows/apps/windows.storage.provider.readactivationmode.aspx) <br/> |Defina **BeforeAccess** para permitir que o seu aplicativo atualizar o arquivo antes de enviá-lo ao escritório.  <br/> |
|[WriteActivationMode](https://msdn.microsoft.com/en-us/library/windows/apps/windows.storage.provider.writeactivationmode.aspx) <br/> |Defina **ReadOnly** para tornar o arquivo somente leitura. Defina **AfterWrite** para garantir que seu aplicativo será acionado pelo CacheFileUpdater quando o Office for concluído com o arquivo.<br/><br/>**Observação**: se você não definir **AfterWrite**, seu aplicativo não será notificado para carregar as alterações, que significa que as alterações do usuário só será locais.           |
|[CachedFileOptions.RequireUpdateOnAccess](https://msdn.microsoft.com/en-us/library/windows/apps/windows.storage.provider.cachedfileoptions.aspx) <br/> |Defina essa propriedade para garantir que o seu aplicativo pode atualizar o arquivo quando um usuário acessa-lo da lista recente.  <br/> |
   
## <a name="invoking-office-from-your-app"></a>Office de invocação do seu aplicativo

Quando um usuário abre um documento do Office a partir de seu aplicativo, o documento pode abrir no Excel Mobile, Mobile do PowerPoint e Word Mobile. Por exemplo, quando um usuário seleciona um \*arquivo. docx no seu aplicativo, o Word Mobile inicia com o \*arquivo. docx aberto. O aplicativo do Office que abre se baseia em qual aplicativo usuário associado com o tipo de arquivo.
  
Para abrir um arquivo do seu aplicativo no escritório, é recomendável que você use **LaunchFileAsync()** para iniciar o arquivo. Não recomendamos que você use **LaunchUriAsync()** para iniciar o arquivo, pois isso fará com que o aplicativo registrado para o esquema de URI para início (o navegador), em vez do Office. Embora **LaunchUriAsync()** com a opção **LauncherOptions.ContentType()** pode chamar Office, neste caso o arquivo aberto está marcado como temporário e é somente leitura no Office. 
  
Para obter mais informações, consulte [classe de iniciador](https://msdn.microsoft.com/en-us/library/windows/apps/windows.system.launcher.aspx).
  
## <a name="temporary-and-read-only-files"></a>Arquivos temporários e somente leitura

Defina o atributo **FILE_ATTRIBUTE_TEMPORARY** arquivos temporários e o atributo **FILE_ATTRIBUTE_READONLY** em arquivos somente leitura em seu aplicativo. 
  
Arquivos com os atributos **FILE_ATTRIBUTE_TEMPORARY** ou **FILE_ATTRIBUTE_READONLY** definir abertos como somente leitura no Office. O **FILE_ATTRIBUTE_TEMPORARY** também impede que o arquivo que aparecem na lista recente. 
  
Para obter mais informações sobre os atributos de arquivo, consulte a [função de SetFileAttributes](https://msdn.microsoft.com/en-us/library/windows/desktop/aa365535%28v=vs.85%29.aspx).
  
## <a name="other-best-practices"></a>Outras práticas recomendadas

Para otimizar a consistência de arquivo, por exemplo quando edições conflitantes ou erros ocorrem, aplique as seguintes práticas recomendadas:
  
- Evitar conflitos de salvamento.
    
  - Pausar carrega quando ocorrem de conflitos de servidor para evitar a bifurcação (somente bifurcação quando o Office não tem mais um arquivo de gravação abrir). Normalmente, se um arquivo do seu aplicativo estiver aberto no Office, seu aplicativo será ativado somente quando o escritório fecha ou está suspenso pelo Windows.
    
  - Se você precisar de UI para lidar com conflitos, implemente notificações da proposta. UI completa não está disponível quando o Office é suspenso.
    
- Lidar com erros.
    
  - Quando um bloqueio for liberado, notificar os usuários sobre o conflito e fornecer um caminho para resolvê-lo no seu aplicativo.
    
## <a name="see-also"></a>Confira também

- [Integração com o Office](integrate-with-office.md)   
- [Integração com o Office de clientes de sincronização de Win32](integrate-with-office-from-win32-sync-clients.md)
    

