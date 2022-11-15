## AutoCrypto
*Применение различных моделей на датасет autocrypto, подбор оптимальных параметров и устройства нейросети*
- [``]() 

Модель 1.1, tensorflow+keras, [перевод](https://habr.com/ru/post/495884/) официальной статьи от TF.
#### Этапы:
- предсказывается spot только по spot'у через определенное время,
- spot по выбранным фичам через определенное время,
- группа spot'ов определенной длины по выбранным фичам.

#### 2 входных датасета:
- 2021-07-10 - дата начала сбора 'total_oi', 'binance_spot_price', 'binance_weighted_acc_ratio', 'binance_weighted_position_ratio', первая группа данных будет содержать строки с timestamp'ом 2021-07-10 - 2022-10-13 (примерно 15 месяцев, 439 наблюдений), 
- 2022-10-14 - дата начала сбора всех данных, вторая группа данных будет содержать строки с timestamp'ом 2022-10-14 - 2022-10-29 (15 дней, 4387 наблюдений).


*tensorflow* 
> tf.data.Dataset.from_tensor_slices(())🦎.cache()🦎.shuffle()🦎.batch()🦎.repeat()🦎tf.keras.models.Sequential()🦎tf.keras.layers.Dense()🦎.take()🦎.predict()🦎.add()🦎.history['']🦎.any()🦎.format()

> tf.keras.layers.LSTM(input_shape = , activation='relu', return_sequences = )

> .compile(optimizer=tf.keras.optimizers.Adam(clipvalue=, learning_rate=) | 'adam' | 'rmsprop' | 'sgd', loss='mse' | 'mae' | 'binary_crossentropy', metrics=['accuracy'])

>.fit(epochs=, steps_per_epoch = , validation_data = , validation_steps = )
