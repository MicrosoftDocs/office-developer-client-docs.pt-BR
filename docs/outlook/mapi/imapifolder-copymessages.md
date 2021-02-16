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
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424452"
---
# <a name="imapifoldercopymessages"></a>IMAPIFolder::CopyMessages

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Um ponteiro para uma matriz de [estruturas ENTRYLIST](entrylist.md) que identificam a mensagem ou mensagens a ser copiadas ou movimentadas. 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a pasta de destino apontada pelo parâmetro _lpDestFolder._ Passar resultados NULL no provedor de serviços retornando a interface de pasta padrão, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Os clientes devem passar NULL. Outros chamadores podem definir o  _parâmetro lpInterface_ como IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer ou IID_IMAPIFolder. 
    
 _lpDestFolder_
  
> [in] Um ponteiro para a pasta aberta para receber as mensagens copiadas ou movidas.
    
 _ulUIParam_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe. O _parâmetro ulUIParam_ é ignorado, a menos que o cliente defina o sinalizador MESSAGE_DIALOG no parâmetro _ulFlags_ e passe NULL no _parâmetro lpProgress._ 
    
 _lpProgress_
  
> [in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso. Se NULL for passado  _em lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação de objeto de progresso MAPI. O  _parâmetro lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG seja definido em  _ulFlags_.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a operação de cópia ou movimentação é realizada. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DECLINE_OK 
  
> Informa o provedor de armazenamento de mensagens para retornar imediatamente MAPI_E_DECLINE_COPY se implementar **IMAPIFolder::CopyMessages** chamando o método [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) ou [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) do objeto de suporte. 
    
MESSAGE_DIALOG 
  
> Exibe um indicador de progresso à medida que a operação prosse passa.
    
MESSAGE_MOVE 
  
> A mensagem ou as mensagens devem ser movidas em vez de copiadas. Se MESSAGE_MOVE não estiver definida, as mensagens serão copiadas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A mensagem ou as mensagens foram copiadas ou movidas com êxito.
    
MAPI_E_DECLINE_COPY 
  
> O provedor implementa esse método chamando um método de objeto de suporte e o chamador passou o sinalizador MAPI_DECLINE_OK suporte.
    
MAPI_W_PARTIAL_COMPLETION 
  
> A chamada foi bem-sucedida, mas nem todas as entradas foram copiadas ou movidas com êxito. Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPIFolder::CopyMessages** copia ou move mensagens para outra pasta. 
  
As mensagens abertas com permissão de leitura/gravação podem ser movidas ou copiadas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se você estiver copiando mensagens para outro armazenamento de mensagens sem usar o método [IMAPISupport::CopyMessages,](imapisupport-copymessages.md) primeiro deverá chamar [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) com o sinalizador GENERATE_RECEIPT_ONLY definido. O armazenamento de mensagens de recebimento não é responsável por gerar relatórios de leitura para as mensagens copiadas ou movidas. Se você estiver chamando **IMAPISupport::CopyMessages** para implementar **IMAPIFolder::CopyMessages**, não chame **SetReadFlags**; O MAPI o chamará. 
  
Sua implementação pode mover ou copiar as mensagens em qualquer ordem e gerar relatórios de status de leitura em qualquer ordem. Ou seja, você pode concluir a cópia de mensagens antes de gerar qualquer um dos relatórios de status de leitura ou enviar os relatórios antes de sua implementação iniciar a operação de cópia. No entanto, relatórios de leitura devem ser enviados para que todas as mensagens sejam copiadas, independentemente de a cópia ter sido bem-sucedida.
  
Quando a operação de cópia ou movimentação envolver mais de uma mensagem, execute a operação o mais completamente possível. Não pare a operação prematuramente, a menos que ocorra uma falha que esteja além do controle, como falta de memória, falta de espaço em disco ou corrupção no armazenamento de mensagens.
  
Tente manter os identificadores de entrada em operações de movimentação ou cópia. Você também deve preservar identificadores de entrada, embora isso não seja necessário.
  
Envie notificações ao mover ou copiar mensagens para que os clientes sejam alertados de que suas chamadas para os métodos [IMAPIProp::SaveChanges](imapiprop-savechanges.md) das mensagens podem falhar. 
  
Não inclua o status de uma mensagem na operação de cópia ou movimentação. Mover ou copiar um status de mensagem afeta muito o desempenho.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Use **IMAPIFolder::CopyMessages** para preencher pastas de resultados de pesquisa, onde as mensagens são frequentemente agrupadas por pasta pai. 
  
Espere esses valores de retorno sob as seguintes condições.
  
|**Condition**|**Valor de retorno**|
|:-----|:-----|
|**IMAPIFolder::CopyMessages** copiou ou moveu todas as mensagens com êxito.  <br/> |S_OK  <br/> |
|**IMAPIFolder::CopyMessages** não pôde copiar ou mover todas as mensagens com êxito.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**IMAPIFolder::CopyMessages** não pôde ser concluída.  <br/> |Qualquer valor de erro  <br/> |
   
Quando **IMAPIFolder::CopyMessages** não puder ser concluída, não suponha que nenhum trabalho foi feito. **IMAPIFolder::CopyMessages** pode ter sido capaz de copiar ou mover uma ou mais mensagens antes de encontrar o erro. 
  
## <a name="see-also"></a>Confira também



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

