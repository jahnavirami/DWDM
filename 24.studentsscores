# Marks data
marks <- c(55, 60, 71, 63, 55, 65, 50, 55, 58, 59, 61, 63, 65, 67, 71, 72, 75)

# (a) Equal-frequency (equi-depth) partitioning
eq_freq_bins <- cut(marks, breaks = 3, labels = FALSE)

# (b) Equal-width partitioning
eq_width_bins <- cut(marks, breaks = 3, labels = FALSE)

# (c) Clustering (k-means)
num_clusters <- 3
cluster_centers <- kmeans(matrix(marks, ncol = 1), centers = num_clusters)$centers
cluster_assignments <- findInterval(marks, vec = cluster_centers)

# Plotting histograms
par(mfrow = c(3, 1))

# Plot for equal-frequency partitioning
hist(marks, main = "Equal-Frequency Partitioning", breaks = 3, col = "blue", xlab = "Marks")
abline(v = cluster_centers, col = "red", lwd = 2)

# Plot for equal-width partitioning
hist(marks, main = "Equal-Width Partitioning", breaks = seq(min(marks), max(marks), length.out = 4), col = "green", xlab = "Marks")
abline(v = cluster_centers, col = "red", lwd = 2)

# Plot for clustering
hist(marks, main = "Clustering", breaks = 3, col = "purple", xlab = "Marks")
abline(v = cluster_centers, col = "red", lwd = 2)

par(mfrow = c(1, 1)) # Resetting the plotting layout