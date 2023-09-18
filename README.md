# Макет LoftHouse, ВебКадеми

## Заметки по проекту

### Новые для меня технологии

1. #### Использование SCSS
   - главный файл main.scss, к которому поключаются остальные: _variables.scss, _base.scss, _blocks.scss;
   - используются амперсанды, но для больших проектов они не удобны: затрудняют поиск по селекторам (block &__element &--modifikator, block &:hover, ...)
   - для каждого блока в классе, названному по БЭМ, свой блок в scss (без исключений);
   - для сниппета ```{", "    ${1}", "};```
      
2. #### Grid
   - ```grid-template-columns: repeat(auto-fit, minmax(290px, 1fr))``` - для адаптивности. (290px = 320px - 15px*2)
  
### Общее по разметке

   - для отсутсвующих в section h2/h3 пишутся заголовки, которые скрываются в классе visually-hidden (для семантики);
   - Пример:  
     весь ::before нужен только, когда есть модификаторы --tel и --map.   
     Поэтому не просто ::before, а --tel, --map::before.  
     Чтобы он не работал просто так, когда нет никаких модификаторов;
   - при нажатии на гамбургер ставить в js класс .no-scroll, в котором будет hidden overflow-y;
   - в reset максимальная ширина картинок 100%;
