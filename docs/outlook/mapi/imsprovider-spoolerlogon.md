---
title: IMSProviderSpoolerLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.SpoolerLogon
api_type:
- COM
ms.assetid: 79d5af23-efad-4013-a330-56babfb2bb0f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 56c025713b0cc2b41a4bf4463f48f8d7c3d2124b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586414"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra o MAPI spooler em um armazenamento de mensagens.
  
```cpp
HRESULT SpoolerLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG cbSpoolSecurity,
  LPBYTE lpbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB     
);
```

## <a name="parameters"></a>Parâmetros

 _lpMAPISup_
  
> [in] Um ponteiro para MAPI suporte ao objeto para o armazenamento de mensagens.
    
 _ulUIParam_
  
> [in] Um identificador para a janela do pai de quaisquer caixas de diálogo ou windows esse método exibe. 
    
 _lpszProfileName_
  
> [in] Um ponteiro para uma cadeia de caracteres que contém o nome do perfil que está sendo usado para o logon de spooler MAPI. Esta cadeia de caracteres pode ser exibida nas caixas de diálogo, gravada em um arquivo de log ou simplesmente ignorada. Ele deve estar no formato Unicode, se o sinalizador MAPI_UNICODE é definido no parâmetro _ulFlags_ . 
    
 _cbEntryID_
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada para o armazenamento de mensagens. Passar NULL no parâmetro _lpEntryID_ indica que um armazenamento de mensagens ainda não foi selecionado e que as caixas de diálogo que permitem que o usuário selecione um armazenamento de mensagens podem ser apresentadas. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o logon é executado. Sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> A chamada será autorizada tenha êxito, mesmo se o objeto subjacente não está disponível para a implementação de chamada. Se o objeto não estiver disponível, uma chamada subsequente ao objeto pode gerar um erro.
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se MAPI_UNICODE não estiver definida, as cadeias de caracteres estão no formato ANSI.
    
MDB_NO_DIALOG 
  
> Impede a exibição das caixas de diálogo de logon. Se esse sinalizador estiver definido, o valor de erro MAPI_E_LOGON_FAILED retornado se o logon for bem sucedido. Se esse sinalizador não estiver definido, o provedor de armazenamento de mensagens pode solicita ao usuário para corrigir um nome ou a senha, insira um disco ou para executar outras ações necessárias para estabelecer a conexão para o repositório.
    
MDB_WRITE 
  
> Permissão de leitura/gravação solicitações.
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) para o armazenamento de mensagens fazer logon. Passar NULL indica que a interface MAPI para o armazenamento de mensagens ([IMsgStore](imsgstoreimapiprop.md)) é retornada. O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface apropriado para o armazenamento de mensagens (por exemplo, IID_IUnknown ou IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> [in] Um ponteiro para o tamanho, em bytes, de dados de validação no parâmetro _lppbSpoolSecurity_ . 
    
 _lpbSpoolSecurity_
  
> [in] Um ponteiro para um ponteiro para validação de dados. O método **SpoolerLogon** usa esses dados para efetuar o MAPI spooler no mesmo armazenamento como o provedor de armazenamento de mensagem anteriormente logon usando o método [IMSProvider::Logon](imsprovider-logon.md) . 
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para a retornado [MAPIERROR](mapierror.md) estrutura, se houver, que contém informações de versão, componente e contexto para um erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** para retornar. 
    
 _lppMSLogon_
  
> [out] Um ponteiro para o ponteiro para a mensagem armazenar o objeto de logon de MAPI fazer logon.
    
 _lppMDB_
  
> [out] Um ponteiro para o ponteiro para a mensagem armazenar o objeto para o spooler MAPI e os aplicativos de cliente para fazer logon.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_UNCONFIGURED 
  
> O perfil não conter informações suficientes para que o logon concluir. Quando este valor é retornado, MAPI chama a função de ponto entrada do serviço de mensagem do provedor de repositório a mensagem.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida, mas o provedor de armazenamento de mensagem tem informações de erro disponíveis. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md). Para obter as informações de erro do provedor, chame o método [IMAPISession::GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Comentários

O MAPI spooler chama o método de **IMSProvider::SpoolerLogon** para fazer logon um armazenamento de mensagens. O MAPI spooler deve usar o objeto de repositório de mensagem retornado pelo provedor de repositório de mensagem no parâmetro _lppMDB_ durante e após o logon. 
  
Para obter consistência com o método [IMSProvider::Logon](imsprovider-logon.md) , o provedor também retorna um objeto de logon do repositório de mensagem no parâmetro _lppMSLogon_ . O uso do objeto store e o objeto de logon são idênticas para logon repositório usual; deve haver uma correspondência direta entre o objeto de logon e o objeto de armazenamento, de forma que os objetos agir como se fossem um objeto que expõe duas interfaces. Os dois objetos são criados juntos e liberação juntos. 
  
O provedor de armazenamento internamente marcará o objeto de repositório de mensagem retornada para indicar que o repositório está sendo usado pelo spooler MAPI. Alguns métodos para este objeto de repositório de forma diferente da mensagem armazenar objeto fornecido aos aplicativos cliente se comportam. Manter este marca interna é a maneira mais comum de disparo o comportamento específico para o spooler MAPI.
  
## <a name="see-also"></a>Confira também



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

