#route file
Api.php

Route::middleware('auth:sanctum')->group(function () {
    Route::apiResource('events', EventController::class);
    Route::post('bookings', [BookingController::class, 'store']);
});

// Public route
Route::post('attendees', [AttendeeController::class, 'store']);
