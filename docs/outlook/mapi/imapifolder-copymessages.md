---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e6e9e9cefc75ffc78ee7beb47e89063ea1a66ce7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766968"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**Aplica-se a**: Outlook 
  
Copia ou move uma ou mais mensagens.
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpMsgList_
  
> [in] Um ponteiro para uma matriz de estruturas [ENTRYLIST](entrylist.md) que identificam a mensagem ou mensagens para copiar ou mover. 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a pasta de destino apontado pelo parâmetro _lpDestFolder_ . Passagem nula resulta em retornando a interface de pasta padrão, o provedor de serviços [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Os clientes devem passar NULL. Outros chamadores podem definir o parâmetro _lpInterface_ IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Um ponteiro para a pasta aberta para receber as mensagens copiadas ou movidas.
    
 _ulUIParam_
  
> [in] Um identificador para a janela do pai de quaisquer caixas de diálogo ou windows esse método exibe. O parâmetro _ulUIParam_ é ignorado, a menos que o cliente define o sinalizador MESSAGE_DIALOG no parâmetro _ulFlags_ e transmite NULL no parâmetro _lpProgress_ . 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG está definido na _ulFlags_.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a operação de cópia ou movimentação é realizada. Sinalizadores a seguir podem ser definidos:
    
MAPI_DECLINE_OK 
  
> Informa o provedor de armazenamento de mensagem para retornar imediatamente MAPI_E_DECLINE_COPY se ele implementa **IMAPIFolder::CopyMessages** chamando o método [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) de suporte do objeto. 
    
MESSAGE_DIALOG 
  
> Exibe um indicador de progresso conforme continua a operação.
    
MESSAGE_MOVE 
  
> A mensagem ou mensagens deverão ser movidos, em vez de copiados. Se MESSAGE_MOVE não estiver definida, as mensagens serão copiadas.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A mensagem ou mensagens foram com êxito copiadas ou movidas.
    
MAPI_E_DECLINE_COPY 
  
> O provedor implemente esse método chamando um método de objeto de suporte e o chamador passou o sinalizador MAPI_DECLINE_OK.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas nem todas as entradas foram copiadas ou movidas com êxito. Quando esse aviso é retornado, a chamada deve ser manipulada com êxito. Para testar esse aviso, use a macro **HR_FAILED** . Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder::CopyMessages** copia ou mova mensagens para outra pasta. 
  
Mensagens que são abertas com leitura/gravação permissão pode ser movido ou copiado. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Se você estiver copiando mensagens para outro repositório de mensagens sem usar o método [IMAPISupport::CopyMessages](imapisupport-copymessages.md) , primeiro você deve chamar [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) com o sinalizador GENERATE_RECEIPT_ONLY definido. O armazenamento de recebimento de mensagens não é responsável por gerar relatórios de leitura para as mensagens copiadas ou movidas. Se você estiver chamando **IMAPISupport::CopyMessages** para implementar **IMAPIFolder::CopyMessages**, não for chamado **SetReadFlags**; MAPI irá chamá-lo. 
  
A implementação pode mover ou copiar as mensagens em qualquer ordem e gerar relatórios de status de leitura em qualquer ordem. Ou seja, você pode concluir copiem mensagens antes de gerar qualquer um dos relatórios de status de leitura ou enviar relatórios antes de sua implementação inicia a operação de cópia. No entanto, ler relatórios devem ser enviados para todas as mensagens a serem copiados, independentemente se a cópia é bem-sucedida.
  
Quando a operação de cópia ou movimentação envolve mais de uma mensagem, execute a operação como completamente. Não interrompa a operação prematuramente, a menos que ocorre uma falha que está fora de seu controle, como ficando sem memória, ficando sem espaço em disco ou corrupção no repositório de mensagem.
  
Tente manter os identificadores de entrada entre as operações de movimentação ou cópia. Você também deve preservar identificadores de entrada, embora não seja obrigatório.
  
Envie notificações quando você mover ou copiar mensagens para que os clientes seja informados de que suas chamadas para métodos de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) das mensagens podem falhar. 
  
Não incluir o status da mensagem na cópia ou operação de movimentação. Mover ou copiar um status de mensagem muito afeta o desempenho.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Use **IMAPIFolder::CopyMessages** para preencher a pastas de resultados da pesquisa, onde as mensagens são frequentemente agrupadas por pasta pai. 
  
Espera esses valores de retorno sob as condições a seguintes.
  
|**Condição**|**Valor retornado**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages** tem copiados ou movidos de cada mensagem com êxito.  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** foi capaz de copiar ou mover todas as mensagens com êxito.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder::CopyMessages** não pôde concluir.  <br/> |Qualquer valor de erro  <br/> |
   
Quando **IMAPIFolder::CopyMessages** é impossível concluir, não presuma que foi feito nenhum trabalho. **IMAPIFolder::CopyMessages** podem ter sido capaz de copiar ou mover uma ou mais mensagens antes da ocorrência de erro. 
  
## <a name="see-also"></a>Confira também



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

