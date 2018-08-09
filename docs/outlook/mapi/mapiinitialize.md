---
title: MAPIInitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIInitialize
api_type:
- HeaderDef
ms.assetid: b9584226-79d2-4d83-8f31-dbfbc50f16c5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d22c24088960debcd18ccd818dad23656f6a01f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768005"
---
# <a name="mapiinitialize"></a>MAPIInitialize

  
  
**Aplica-se a**: Outlook 
  
Incrementa a contagem de referência do subsistema MAPI e inicializa dados globais para a DLL de MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HRESULT MAPIInitialize(
  LPVOID lpMapiInit
);
```

## <a name="parameters"></a>Parâmetros

 _lpMapiInit_
  
> [in] Ponteiro para uma estrutura [MAPIINIT_0](mapiinit_0.md) . O parâmetro _lpMapiInit_ pode ser definido como NULL. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O subsistema de MAPI foi inicializado com êxito.
    
## <a name="remarks"></a>Comentários

Os incrementos de função **MAPIInitialize** a MAPI contagem de referência para o subsistema de MAPI e o diminui de função [MAPIUninitialize](mapiuninitialize.md) a interna contagem de referência. Assim, o número de chamadas para uma função deve ser igual o número de chamadas para outro. **MAPIInitialize** Retorna S_OK se MAPI não foi inicializado anteriormente. 
  
Um provedor de cliente ou serviço deve chamar **MAPIInitialize** antes de fazer qualquer outra chamada MAPI. Falha ao fazer isso faz com que o cliente ou serviço de chamadas do provedor retornar o valor MAPI_E_NOT_INITIALIZED. 
  
Ao chamar **MAPIInitialize** de um aplicativo multithreaded, defina o parâmetro _lpMapiInit_ para uma estrutura [MAPIINIT_0](mapiinit_0.md) que é declarada como se segue: 
  
 **MAPIINIT_0** MAPIINIT = {0, MAPI_MULTITHREAD_NOTIFICATIONS} 
  
e a chamada: 
  
 **MAPIInitialize** (&amp;MAPIINIT); 
  
Quando essa estrutura é declarada, MAPI cria um segmento separado para manipular a janela de notificação, que continua até que a contagem de referência initialize cai para zero. Um serviço do Windows deve definir o membro **ulflags** da estrutura **MAPIINIT_0** apontado pela _lpMapiInit_ para MAPI_NT_SERVICE. 
  
> [!NOTE]
> Você não pode chamar **MAPIInitialize** ou **MAPIUninitialize** de dentro de uma função do Win32 **DllMain** ou qualquer outra função que cria ou finaliza threads. Para obter mais informações, consulte [Usando objetos de Thread-Safe](using-thread-safe-objects.md). 
  
 **MAPIInitialize** não devolvem nenhuma informação de erro estendidas. Ao contrário da maioria das outras chamadas MAPI, os significados de seus valores de retorno estritamente são definidos para corresponder à etapa específica da inicialização que falharam: 
  
1. Verifica os parâmetros e os sinalizadores.
    
    MAPI_E_INVALID_PARAMETER ou MAPI_E_UNKNOWN_FLAGS. Chamador passou um parâmetro ou sinalizador inválido.
    
2. Inicializa chaves do registro necessárias pelo MAPI e confirma o tipo de sistema operacional. Esta etapa ocorre apenas se o processo do cliente está sendo executado como um serviço no Windows e define o sinalizador de serviço de MAPI_NT na estrutura **MAPIINIT_0** . 
    
    MAPI_E_TOO_COMPLEX. O processo de chamada é um serviço do Windows e chaves do registro necessárias pelo MAPI não pôde ser inicializadas. 
    
    Informações adicionais podem estar disponíveis no log de eventos do aplicativo.
    
3. Verificar a compatibilidade do MAPI com OLE e inicializar OLE.
    
1. Verifica a compatibilidade entre as versões atuais dos OLE e MAPI. 
    
    MAPI_E_VERSION. A versão do OLE instalada na estação de trabalho não é compatível com esta versão do MAPI.
    
2. Inicializa OLE. 
    
    Durante esta etapa somente, essa função pode retornar um código de erro não listado aqui. Qualquer erro _não_ listado aqui deve ser adotada para a função OLE **CoInitialize**são provenientes.
    
4. Inicializa variáveis globais por processo.
    
    MAPI_E_SESSION_LIMIT. MAPI configura contexto específica para o processo atual. Podem ocorrer falhas Win16 se um determinado número de exceder o número de processos, ou em qualquer sistema se for esgotada a memória disponível.
    
5. Inicializa compartilhadas variáveis globais de todos os processos.
    
    MAPI_E_NOT_ENOUGH_RESOURCES. Recursos do sistema insuficientes estavam disponíveis para concluir a operação.
    
6. Inicializa o mecanismo de notificação, cria sua janela e seu thread se solicitado pelo sinalizador de MAPI_MULTITHREAD_NOTIFICATIONS. 
    
    MAPI_E_INVALID_OBJECT. Pode falhar se os recursos do sistema são esgotados. 
    
7. Carrega e inicializa o provedor de perfil. Verifica se **MAPIInitialize** pode acessar a chave do registro onde estão armazenados os dados de perfil. 
    
    MAPI_E_NOT_INITIALIZED. O provedor de perfil encontrou um erro. 
    
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> ||MFCMAPI usa o método **MAPIInitialize** para inicializar MAPI em um segmento de plano de fundo fazer algumas processamento da tabela.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

