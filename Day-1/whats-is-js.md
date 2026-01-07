# What's is JS?

JavaScript é uma linguagem de programação multi-paradigma (funcional, orientada a objetos e imperativa) onde todos os paradigmas podem ser usados em paralelo, sem a necessidade de uma pré-definição de com qual seguir no inicio do projeto.

A linguagem tem 3 pilares (que serão vistos mais a frente):
- escopes/closures
- prototypes/objects
- types/coercion

## Origem:
Criada por um dev da NetScape (não lembro o nome), com codinome mocha e internamente o nome era LiveScript, quando liberada ao publico o nome JavaScript foi escolhido para chamar atenção dos desenvolvedores Java, e script era a palavra usada para definir programas leves.

## Similaridade com Java:
Não compartilham codebase, as similaridades se devem a tentativa de se aproximas do C/C++ para facilitar a adoção por parte dos devs.

## Especificação:
Existe um comitê responsável pelas alterações no javascript, esse comitê é composto por entre 50 e 100 pessoas de grandes empresas como Google, Apple, Mozilla, etc.
O comitê se compromete com a retrocompatibilidade da linguagem, dito isso, salvo raras excessões, features antiga do JS são sempre suportadas em novas versões da especificação. Quando é necessários fazer alguma alteração, normalmente é considerado se a feature tem baixa adoção, para evitar quebras na web.

A especificação passa por 5 estágios (0 a 4) de aprovação, 0 significa que algum dos membros do comitê aceitou a ideia e pretende trabalhar nela. 4 é quando a feature ja pode ser incluída na próxima revisão da especificação (anualmente).

## Adoção:
As marcas responsáveis pelos motores JS (navegadores/node) se comprometem a implementar a especificação sem alterações de especificação. O tempo de adoção de features não é definido, portando um navegador pode ou não incluir uma feature, mas sempre que incluir ela deverá funcionar de acordo com a especificação.

Como o JS é principalmente usado na WEB, durante a especificação se houver algum conflito o que os navegadores ja utilizam (códigos antigos antes da padronização ou APIs internas usadas pelos browsers), o comitê normalmente prioriza manter o que os browsers ja utilizam e usam uma alternativa na linguagem.

Quando existe alguma diferença entre as features da spec e alguma feature dedicada aos browser, ela é incluída no apêndice B do ECMA. Sendo os apêndices B1 e B3 os que incluem features adicionais e o B3 features conflitantes.

## Compatibilidade Futura:
O JS não tem compatibilidade futura, o que significa que uma engine antiga provavelmente não irá executar uma versão mais recente da linguagem.
Isso não é motivo para escrever código utilizando versões antigas da especificação.
Devemos resolver isso com o uso de transpilers.

### Transpilers:
São ferramentas responsáveis por converter código moderno em código JS compatível com versões mais antigas. Nesse tipo de ferramenta o dev define até qual versão ele quer ter compatibilidade e a ferramenta transforma o código em versões compatíveis.

### Polyfill:
Quando uma API nova não está disponível em uma engine, podemos usar um polyfill. A ideia dessa técnica é criar um equivalente da API com código compatível. 