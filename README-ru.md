<div  align="left">
English: <a  title="English"  href="README.md"><img  src="https://upload.wikimedia.org/wikipedia/commons/a/ae/Flag_of_the_United_Kingdom.svg"  height="11px"/></div>

# Тестер портов USB
![alt text](https://github.com/g42/USB-Tester/blob/main/images/tester_2.4-sch-2.png)

Данный тестер совмещает в себе две функции:
* Проверка сигнальных линий порта USB на
наличие короткого замыкания или заниженного сопротивления.
* Индикация инициализации устройства, по шине USB.

Тестер показывает инициализацию даже при отсутствии вывода
изображения, но при исправном процессоре, хабе, памяти и BIOS.
Если в компьютере неисправна видеосистема, экран и канал вывода
видеосигнала, то тестер покажет инициализацию. Также это
позволяет тестировать системные платы без сборки устройства и
подключения экрана.

При подключении тестера в порт выключенного устройства с нормальным сопротивлением линий - тестер остается в спящем режиме до появления питания на
шине USB. При появлении питания - тестер начинает медленно
моргать индикатором INIT. После успешной инициализации и опроса
шины USB тестер издает короткий писк и индикатор INIT начинает
моргать быстро. 

После инициализации на индикатор SHORT дублируется индикатор NUM
LOCK. Это позволяет убедится в корректной работе USB:
переключите режим NUM LOCK с клавиатуры - тестер покажет
активен ли режим в данный момент. Специальных драйверов не
требуется — тестер эмулирует стандартную HID клавиатуру.

По
умолчанию тестер эмулирует периодическое нажатие кнопки CAPS
LOCK, что позволяет контролировать "зависание" устройства по
мерцанию индикатора CAPS LOCK на клавиатуре. Моргание CAPS
можно отключить нажатием кнопки на тестере (при подключенном
тестере). Повторное нажатие эмулирует набор теста. Нажмите кнопку
еще раз, чтобы вернуться в режим мигания CAPS LOCK.

Проверка на наличие КЗ осуществляется автоматически, при
подключении тестера к разъему USB. При наличии КЗ тестер издает
непрерывный звуковой сигнал и зажигает индикатор "SHORT".
Это позволяет быстро произвести первичную диагностику хаба (PCH)
или, например, процессора U-серии со встроенным хабом. При этом,
перед индикацией есть небольшая задержка (менее 1 сек), это
необходимо для зарядки паразитной емкости линии и исключения
ложного срабатывания. При нормальном сопротивлении линий — тестер остается в спящем
режиме. Индикаторы при этом не задействованы.

Так как, в большинстве случаев, при неисправном USB, напряжение
питания на портах USB отсутствует, тестер имеет встроенный
аккумулятор, который необходим для замера сопротивления на
сигнальных линиях. Его зарядка возможна от любого подходящего
БП или от тестируемого устройства, при наличии 5В на разъеме USB.
Время полного заряда около 1 часа. В нерабочем состоянии (когда
тестер никуда не подключен) заряд не расходуется. Предусмотрена
индикация заряда аккумулятора, для проверки нажмите кнопку на
тестере. Последует 1 короткий писк и 1 мигание INIT - заряд батареи в
норме. Либо 3 коротких писка и 1 мигание SHORT - батарея
разряжена. Если реакции на кнопку нет - батарея в глубоком разряде,
либо тестер неисправен. При низком заряде батареи возможен
некорректный замер сопротивления.

Защитная оболочка тестера защищает проверяемый компьютер и
компоненты тестера от попадания статики на сигнальные шины.
Также, предусмотрена защита USBLC6.
Ширина тестера 17 мм, что позволяет использовать рядом
расположенные разъемы USB для подключения других устройств.

По любым вопросам, обращайтесь по электронной почте <a href="mailto:20kohm@gmail.com">20kohm@gmail.com</a>