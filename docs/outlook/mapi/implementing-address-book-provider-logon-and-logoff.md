---
title: Implementar o logon e logoff do provedor do catálogo de endereços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f26e7b7ec607c9714012870d5367a0e775c62f34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572099"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Implementar o logon e logoff do provedor do catálogo de endereços

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de catálogo de endereços oferecem suporte a sessão logon e logoff Implementando os métodos para o [IABProvider: IUnknown](iabprovideriunknown.md) interface. O * * IABProvider * * interface herda diretamente da **IUnknown** e adiciona apenas dois outros métodos: **Logon** e **desligamento**. 
  
## <a name="logoff"></a>Fazer logoff

MAPI chamará o método [IABProvider::Logon](iabprovider-logon.md) do seu provedor de serviço no início de cada sessão e sempre que o seu provedor é adicionado ao perfil atual e o cliente oferece suporte a reconfiguração dinâmica. Quando MAPI chama o método **IABProvider::Logon** , seu provedor de catálogo de endereços começa seu processo de logon. 
  
**Para implementar IABProvider::Log**
  
1. Inicialize todos os ponteiros de parâmetro de saída passados por MAPI. 
    
2. Chame o suporte ao método do objeto **AddRef** para incrementar sua contagem de referência. 
    
3. Chame o suporte ao método do objeto [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para abrir a seção do perfil que contém informações sobre o seu provedor de configuração. Passe nulo para o parâmetro _lpUID_ e o sinalizador MAPI_MODIFY se você pretende fazer alterações. 
    
4. Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) da seção perfil para recuperar as propriedades que precisa de seu provedor de logon, como o nome da tabela de banco de dados ou arquivo de dados. 
    
5. Verifique se as propriedades estão todos disponíveis e válido. Se necessário e permitidos, exibe uma caixa de diálogo para solicitar que o usuário faça correções ou adições à informações ausentes ou inválidas e chamar o método de [IMAPIProp::SetProps](imapiprop-setprops.md) da seção perfil para salvar as alterações. Algumas das propriedades comuns que deveriam estar disponíveis incluem: 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > Não defina **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ou **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)). Ao fazer logon, essas propriedades são somente leitura. 
  
6. Se uma ou mais propriedades de configuração não estiverem disponíveis, falhar e retornar o valor MAPI_E_UNCONFIGURED.
    
7. Chame [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar um [MAPIUID](mapiuid.md). Seu provedor pode criar um **MAPIUID** por: 
    
   - Chamando o método [IMAPISupport::NewUID](imapisupport-newuid.md) . 
    
   - Chamar o UUIDGEN. Ferramenta EXE para definir um GUID que seu provedor usa para incluir em um dos seus arquivos de cabeçalho.
    
8. Se preferir, salve um recém-criado **MAPIUID** no perfil atual chamando-se a seção de perfil * * IMAPIProp::SetProps * * método. 
    
9. Libere a seção perfil chamando seu método **IUnknown:: Release** . 
    
10. Criar uma instância de um novo objeto de logon e defina o conteúdo do parâmetro _lppABLogon_ como o endereço desse novo objeto. 
    
Porque é possível de MAPI chamar seu * * Logon * * método várias vezes durante uma sessão, é recomendável suportar essa possibilidade em sua implementação por ser capaz de criar vários objetos de logon e manter um registro de cada objeto é criado. Suporte a várias chamadas de **Logon** permite que um usuário de um aplicativo cliente, por exemplo, para fazer logon em uma sessão com diferentes identidades ou destinos de entrega diferente de uso. 
  
**Desligamento** é chamado quando a sessão está terminando. MAPI chama seu método [IABProvider::Shutdown](iabprovider-shutdown.md) como uma das últimas tarefas envolvidas na desligando a uma sessão. MAPI lançou todos os objetos de logon do seu provedor e, quando o seu provedor recebe essa chamada, ele pode assumir que esta é a última chamada, que ele receberá. Na sua implementação do **IABProvider::Shutdown**, execute qualquer limpeza final que você acha que é necessário. Por exemplo, seu provedor pode chamar **MAPIDeinitIdle** se ele tiver chamado **MAPIInitIdle** para usar o mecanismo de ociosidade durante a sessão ou o método **IUnknown:: Release** todos os objetos que ainda precisam ser liberada. 
  
Se o seu provedor não tem nenhuma limpeza final, sua implementação pode ser constituída de uma única linha de código: 
  
```cpp
return S_OK;

```


