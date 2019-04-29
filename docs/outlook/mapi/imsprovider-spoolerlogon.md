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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 794674df38266743cac8c947ec93dc1fcfff438b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430571"
---
# <a name="imsproviderspoolerlogon"></a>IMSProvider::SpoolerLogon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra o spooler MAPI em um repositório de mensagens.
  
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
  
> no Um ponteiro para o objeto de suporte MAPI para o repositório de mensagens.
    
 _ulUIParam_
  
> no Uma alça para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido. 
    
 _lpszProfileName_
  
> no Um ponteiro para uma cadeia de caracteres que contém o nome do perfil que está sendo usado para o logon do spooler MAPI. Essa cadeia de caracteres pode ser exibida em caixas de diálogo, gravadas em um arquivo de log ou simplesmente ignorada. Ele deve estar no formato Unicode se o sinalizador MAPI_UNICODE estiver definido no parâmetro _parâmetroulflags_ . 
    
 _cbEntryID_
  
> no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada para o repositório de mensagens. Passar NULL no parâmetro _lpEntryID_ indica que um repositório de mensagens ainda não foi selecionado e que as caixas de diálogo que permitem ao usuário selecionar um repositório de mensagens podem ser apresentadas. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o logon é executado. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> A chamada terá permissão para ter êxito, mesmo se o objeto subjacente não estiver disponível para a implementação de chamada. Se o objeto não estiver disponível, uma chamada subsequente para o objeto poderá gerar um erro.
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se MAPI_UNICODE não for definido, as cadeias de caracteres estarão no formato ANSI.
    
MDB_NO_DIALOG 
  
> Impede a exibição de caixas de diálogo de logon. Se esse sinalizador estiver definido, o valor de erro MAPI_E_LOGON_FAILED será retornado se o logon não tiver êxito. Se esse sinalizador não for definido, o provedor de armazenamento de mensagens poderá solicitar que o usuário corrija um nome ou senha, insira um disco ou execute outras ações necessárias para estabelecer conexão com o repositório.
    
MDB_WRITE 
  
> Solicita permissão de leitura/gravação.
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) do repositório de mensagens para fazer logon no. Passar NULL indica que a interface MAPI para o repositório de mensagens ([IMsgStore](imsgstoreimapiprop.md)) é retornada. O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o repositório de mensagens (por exemplo, IID_IUnknown ou IID_IMAPIProp). 
    
 _cbSpoolSecurity_
  
> no Um ponteiro para o tamanho, em bytes, dos dados de validação no parâmetro _lppbSpoolSecurity_ . 
    
 _lpbSpoolSecurity_
  
> no Um ponteiro para um ponteiro para dados de validação. O método **SpoolerLogon** usa esses dados para registrar o spooler MAPI no mesmo repositório do que o provedor de armazenamento de mensagens fez logon anteriormente usando o método [IMSProvider:: logon](imsprovider-logon.md) . 
    
 _lppMAPIError_
  
> bota Um ponteiro para um ponteiro para a estrutura [MAPIERROR](mapierror.md) retornada, se houver, que contenha informações de versão, componente e contexto de um erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** a ser retornada. 
    
 _lppMSLogon_
  
> bota Um ponteiro para o ponteiro para o objeto de logon do repositório de mensagens para MAPI para fazer logon no.
    
 _lppMDB_
  
> bota Um ponteiro para o ponteiro para o objeto do repositório de mensagens para o spooler MAPI e aplicativos cliente para fazer logon no.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_UNCONFIGURED 
  
> O perfil não contém informações suficientes para que o logon seja concluído. Quando esse valor é retornado, MAPI chama a função de ponto de entrada do serviço de mensagem do provedor de repositório de mensagens.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada teve êxito, mas o provedor do repositório de mensagens tem informações de erro disponíveis. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md). Para obter as informações de erro do provedor, chame o método [IMAPISession:: GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IMSProvider:: SpoolerLogon** para fazer logon em um repositório de mensagens. O spooler MAPI deve usar o objeto de repositório de mensagens retornado pelo provedor de armazenamento de mensagens no parâmetro _lppMDB_ durante e após o logon. 
  
Para consistência com o método [IMSProvider:: logon](imsprovider-logon.md) , o provedor também retorna um objeto de logon do repositório de mensagens no parâmetro _lppMSLogon_ . O uso do objeto Store e o objeto logon são idênticos para logon de loja usual; deve haver uma correspondência de um para um entre o objeto de logon e o objeto Store, de forma que os objetos atuem como se fossem um objeto que expõe duas interfaces. Os dois objetos são criados juntos e liberados juntos. 
  
O provedor de repositório deve marcar internamente o objeto de repositório de mensagens retornado para indicar que o repositório está sendo usado pelo spooler MAPI. Alguns dos métodos para esse objeto de armazenamento se comportam de forma diferente do objeto do repositório de mensagens fornecido para aplicativos cliente. Manter essa marca interna é a maneira mais comum de acionar o comportamento específico para o spooler MAPI.
  
## <a name="see-also"></a>Confira também



[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIERROR](mapierror.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

