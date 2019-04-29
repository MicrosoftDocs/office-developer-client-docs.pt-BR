---
title: Documentação do valor de retorno MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5bbafe9fda479d951bb20175ab904dc6e241226a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429688"
---
# <a name="mapi-return-value-documentation"></a>Documentação do valor de retorno MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As entradas de referência nesse documento de referência apenas os valores de retorno que exigem algum tratamento por aplicativos cliente. Valores de retorno que indicam condições de erro comuns e podem ser deduzidos verificando se há falha não estão incluídos na documentação. Por exemplo, muitos métodos de interface podem retornar MAPI_E_INVALID_PARAMETER se um chamador especifica o valor incorreto para um parâmetro de entrada. Esse valor normalmente não é listado no conjunto de valores de retorno esperados porque não há necessidade de procurar MAPI_E_INVALID_PARAMETER e não precisa processá-lo de forma diferente de qualquer outro erro. Por outro lado, alguns provedores de serviços não dão suporte à notificação de eventos e retornarão MAPI_E_NO_SUPPORT para o método **Advise** feito pelos clientes por meio do **IMAPISession**. Como os clientes precisam verificar explicitamente esse valor e fornecer código para lidar com a condição que ele representa, deve ocorrer, MAPI_E_NO_SUPPORT está incluído na lista de valores de retorno para [IMAPISession:: Advise](imapisession-advise.md).
  
A tabela a seguir descreve os valores de erro que normalmente são retornados de métodos e funções e exigem manipulação explícita na parte de um cliente ou provedor de serviços. Esses valores se enquadram em quatro categorias: valores que indicam dados de entrada inválidos, valores que indicam problemas de recurso, valores que indicam incompatibilidade de conjunto de caracteres e valores que indicam falha de uma origem desconhecida.
  
|**Valor retornado**|**Descrição**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Um ou mais dos parâmetros passados para o método ou funções não foram válidos.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Um ou mais valores para um parâmetro flags não eram válidos.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Houve um problema ao gravar ou ler do disco.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |Não há espaço em disco suficiente disponível para concluir a operação.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |Memória insuficiente disponível para concluir a operação.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |Não há recursos de sistema suficientes disponíveis para concluir a operação.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |Há uma incompatibilidade nos conjuntos de caracteres com suporte no chamador e na implementação.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Ocorreu um erro de origem inesperada ou desconhecida.  <br/> |
   
As constantes que representam os valores de retorno MAPI estão listadas no MAPICODE. Arquivo de cabeçalho H. Algumas das constantes mapeiam para erros Win32; o mapeamento dessas constantes para valores numéricos pode ser encontrado no arquivo de cabeçalho Win32, WINERROR. 0.
  
Os erros referentes a dados inválidos passados por um chamador podem ser determinados por meio das funções da API de validação de parâmetro fornecidas pelo MAPI ou por um conjunto de macros. 
  
A incompatibilidade de conjunto de caracteres surge quando ocorre uma das seguintes situações:
  
- Um cliente ou um provedor de serviços define o sinalizador MAPI_UNICODE em uma chamada de método ou função e a implementação não dá suporte a Unicode. A definição de MAPI_UNICODE indica que as cadeias de caracteres passadas como entrada são cadeias de caracteres Unicode e que as cadeias de caracteres passadas de volta à medida que a saída deve ser cadeias
    
- Um cliente ou um provedor de serviços não define o sinalizador MAPI_UNICODE em uma chamada de método ou função e a implementação só oferece suporte a Unicode.
    

